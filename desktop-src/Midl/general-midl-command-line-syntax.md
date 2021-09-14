---
title: Sintaxis general de la línea de comandos de MIDL
description: El compilador MIDL procesa un archivo IDL y un archivo de configuración de aplicación (ACF) opcional para generar un conjunto de archivos de salida.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- referencia de línea de comandos MIDL, sintaxis general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159577"
---
# <a name="general-midl-command-line-syntax"></a>Sintaxis general de la línea de comandos de MIDL

El compilador MIDL procesa un archivo IDL y un archivo de configuración de aplicación (ACF) opcional para generar un conjunto de archivos de salida. Los atributos especificados en la lista de atributos de interfaz del archivo IDL determinan si el compilador genera archivos de origen para una interfaz RPC o para una interfaz OLE personalizada.

## <a name="switch-options"></a>Cambiar opciones

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*
</dt> <dd>

Especifica modificadores de línea de comandos del compilador MIDL. Los modificadores pueden aparecer en cualquier secuencia.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*
</dt> <dd>

Especifica las opciones asociadas a cada modificador. Las opciones válidas se describen en la entrada de referencia de cada modificador del compilador MIDL.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Especifica el nombre del archivo IDL. Este archivo normalmente tiene la extensión .idl, pero puede tener otro o ninguno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En las listas siguientes se muestran los nombres predeterminados de los archivos generados para un archivo IDL denominado Name.idl. Puede usar modificadores de línea de comandos para invalidar estos nombres predeterminados. Tenga en cuenta que el nombre del archivo IDL puede tener una extensión que no sea .idl o ninguna extensión.

De forma predeterminada (es decir, si la [](object.md) lista de atributos de interfaz no contiene el objeto o atributo [**local),**](local.md) el compilador genera los siguientes archivos para una [interfaz RPC](files-generated-for-an-rpc-interface.md):

-   Código auxiliar de cliente (nombre \_ c.c)
-   Código auxiliar del servidor \_ (nombre s.c)
-   Archivo de encabezado (name.h)

Cuando el [**atributo de**](object.md) objeto aparece en la lista de atributos de interfaz, el compilador genera los siguientes archivos para una interfaz COM:

-   Archivo de proxy de interfaz \_ (nombre p.c)
-   Archivo de encabezado de interfaz (name.h)
-   Archivo UUID de interfaz (nombre \_ I.c)

Cuando el [**atributo local**](local.md) aparece en la lista de atributos de interfaz, el compilador genera solo el archivo de encabezado de interfaz, Name.h.

El compilador MIDL proporcionado con RPC de Microsoft invoca el preprocesador de C según sea necesario para procesar el archivo IDL. No invoca automáticamente el compilador de C para compilar los archivos generados.

> [!Note]  
> El compilador MIDL proporcionado con RPC de Microsoft usa una sintaxis de línea de comandos diferente a la del compilador de IDL de DCE.

 

Los modificadores del compilador [**MIDL /env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del servidor.

A partir de la versión 6.0.359 de MIDL, la opción de línea de comandos predeterminada para el compilador de MIDL es [**/Oicf**](-oi.md)Â [**/robust**](-robust.md). Para deshabilitar /robust, especifique la [**opción /no \_ robust.**](-no-robust.md)

## <a name="the-header-file"></a>El archivo de encabezado

El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declaradas en el archivo IDL. Todos los módulos de aplicación que llaman a las operaciones definidas, implementan las operaciones definidas o manipulan los tipos definidos deben incluir el archivo de encabezado.

Los modificadores del compilador [**MIDL /header**](-header.md) [**y /out**](-out.md) afectan al archivo de encabezado.

 

 




