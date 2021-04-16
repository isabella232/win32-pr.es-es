---
title: Compilación de MIDL
description: Compilación de MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488334"
---
# <a name="midl-compilation"></a>Compilación de MIDL

Dado un archivo IDL, como [Example2. idl](anatomy-of-an-idl-file.md), que define una o más interfaces com y una biblioteca de tipos, el compilador de MIDL (Midl.exe) genera los archivos que se describen en la tabla siguiente como la salida predeterminada.



| Nombre de archivo                 | Descripción                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Example2. h<br/>    | El archivo de encabezado, que contiene definiciones de tipos y declaraciones de función para todas las interfaces definidas en el archivo IDL, así como declaraciones adelantadas para las rutinas a las que llama el código auxiliar.<br/> |
| Example2 \_ p. c<br/> | El archivo de proxy/código auxiliar, que incluye los puntos de entrada suplentes tanto para los clientes como para los servidores.<br/>                                                                                           |
| Example2 \_ c<br/> | El archivo de identificador de interfaz, que define el GUID para cada interfaz especificada en el archivo IDL.<br/>                                                                                               |
| Example2. tlb<br/>  | Archivo de documento compuesto que contiene información sobre tipos y objetos.<br/>                                                                                                                |
| Dlldata. c<br/>     | Contiene los datos que necesita para crear un archivo DLL de proxy/código auxiliar.<br/>                                                                                                                                     |



 

Use el archivo de encabezado y todos los archivos. c para [crear un archivo dll de proxy](building-and-registering-a-proxy-dll.md) que pueda admitir la interfaz cuando lo usen las aplicaciones cliente y los servidores de objetos. El archivo de encabezado de interfaz (Example2. h) y el archivo de identificador de interfaz (Example2 \_ i. c) se usan al crear el archivo ejecutable para una aplicación cliente que utiliza la interfaz. Puede optar por incluir el archivo de biblioteca de tipos como un recurso en el archivo EXE o DLL, o bien puede enviarlo como un archivo independiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos generados para una interfaz COM](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Opciones del compilador de MIDL](midl-compiler-options.md)
</dt> </dl>

 

