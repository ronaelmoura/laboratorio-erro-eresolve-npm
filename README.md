# Laboratório ERESOLVE do npm

Projeto criado para demonstrar como identificar e corrigir o erro:

ERESOLVE unable to resolve dependency tree

## Problema reproduzido

O projeto utiliza:

- React 18.2.0
- React DOM 18.2.0

O conflito é criado ao tentar instalar:

- react-quill 1.3.5

Essa versão antiga declara compatibilidade com versões de React que chegam apenas até React 16.

## Comandos utilizados

```powershell
npm.cmd install --save-exact react@18.2.0 react-dom@18.2.0

npm.cmd install --save-exact react-quill@1.3.5

npm.cmd view react-quill@1.3.5 peerDependencies
npm.cmd view react-quill@2.0.0 peerDependencies

npm.cmd install --save-exact react-quill@2.0.0

npm.cmd ls react react-dom react-quill
