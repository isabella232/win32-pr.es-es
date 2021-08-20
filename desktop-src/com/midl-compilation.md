---
title: Compilación midl
description: Compilación midl
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a94f94122aeeb1f2900c3adec7e567c794f31ee22259f657dfe5e95f3f688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047953"
---
# <a name="midl-compilation"></a>Compilación midl

Dado un archivo IDL, como [Example2.idl](anatomy-of-an-idl-file.md), que define una o varias interfaces COM y una biblioteca de tipos, el compilador midl (Midl.exe) genera los archivos descritos en la tabla siguiente como salida predeterminada.



| Nombre de archivo                 | Descripción                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ejemplo 2.h<br/>    | El archivo de encabezado, que contiene definiciones de tipo y declaraciones de función para todas las interfaces definidas en el archivo IDL, así como declaraciones de reenvío para las rutinas a las que llaman los códigos auxiliares.<br/> |
| Ejemplo 2 \_ p.c<br/> | El archivo proxy/stub, que incluye los puntos de entrada suplentes tanto para los clientes como para los servidores.<br/>                                                                                           |
| Ejemplo 2 \_ i.c<br/> | Archivo de identificador de interfaz, que define el GUID para cada interfaz especificada en el archivo IDL.<br/>                                                                                               |
| Ejemplo 2.tlb<br/>  | Archivo de documento compuesto que contiene información sobre tipos y objetos.<br/>                                                                                                                |
| Dlldata.c<br/>     | Contiene los datos que necesita para crear un archivo DLL de proxy o de código auxiliar.<br/>                                                                                                                                     |



 

Use el archivo de encabezado y todos los archivos .c para crear un [archivo DLL](building-and-registering-a-proxy-dll.md) de proxy que pueda admitir la interfaz cuando lo usen las aplicaciones cliente y los servidores de objetos. Use el archivo de encabezado de interfaz (Example2.h) y el archivo de identificador de interfaz (Example2 i.c) al crear el archivo ejecutable para una aplicación cliente que \_ usa la interfaz . Puede optar por incluir el archivo de biblioteca de tipos como un recurso en el archivo EXE o DLL, o bien puede enviarlo como un archivo independiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos generados para una interfaz COM](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Opciones del compilador MIDL](midl-compiler-options.md)
</dt> </dl>

 

