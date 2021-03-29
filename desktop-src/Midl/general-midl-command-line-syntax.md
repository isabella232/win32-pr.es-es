---
title: Sintaxis de línea de comandos de MIDL general
description: El compilador MIDL procesa un archivo IDL y un archivo de configuración de la aplicación (ACF) opcional para generar un conjunto de archivos de salida.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- referencia de la línea de comandos MIDL, sintaxis general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903824"
---
# <a name="general-midl-command-line-syntax"></a>Sintaxis de línea de comandos de MIDL general

El compilador MIDL procesa un archivo IDL y un archivo de configuración de la aplicación (ACF) opcional para generar un conjunto de archivos de salida. Los atributos especificados en la lista de atributos de interfaz del archivo IDL determinan si el compilador genera archivos de origen para una interfaz RPC o para una interfaz OLE personalizada.

## <a name="switch-options"></a>Opciones de conmutador

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*modificador de línea de comandos*
</dt> <dd>

Especifica los modificadores de la línea de comandos del compilador de MIDL. Los modificadores pueden aparecer en cualquier secuencia.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*Switch-Options*
</dt> <dd>

Especifica las opciones asociadas a cada modificador. Las opciones válidas se describen en la entrada de referencia para cada conmutador de compilador de MIDL.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extensión*
</dt> <dd>

Especifica el nombre del archivo IDL. Normalmente, este archivo tiene la extensión. idl, pero puede tener otro o ninguno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En las listas siguientes se muestran los nombres predeterminados de los archivos generados para un archivo IDL denominado Name. idl. Puede usar modificadores de la línea de comandos para invalidar estos nombres predeterminados. Tenga en cuenta que el nombre del archivo IDL puede tener una extensión que no sea. idl o ninguna extensión.

De forma predeterminada (es decir, si la lista de atributos de interfaz no contiene el [**objeto**](object.md) o el atributo [**local**](local.md) ), el compilador genera los siguientes archivos para una [interfaz RPC](files-generated-for-an-rpc-interface.md):

-   Código auxiliar de cliente (nombre \_ c. c)
-   Código auxiliar de servidor (name \_ s. c)
-   Archivo de encabezado (Name. h)

Cuando el atributo de [**objeto**](object.md) aparece en la lista de atributos de interfaz, el compilador genera los siguientes archivos para una interfaz com:

-   Archivo de proxy de interfaz (nombre \_ p. c)
-   Archivo de encabezado de interfaz (Name. h)
-   Archivo UUID de interfaz (nombre \_ I. c)

Cuando el atributo [**local**](local.md) aparece en la lista de atributos de interfaz, el compilador genera solo el archivo de encabezado de interfaz, Name. h.

El compilador MIDL proporcionado con Microsoft RPC invoca el preprocesador de C según sea necesario para procesar el archivo IDL. No invoca automáticamente el compilador de C para compilar los archivos generados.

> [!Note]  
> El compilador MIDL proporcionado con Microsoft RPC utiliza una sintaxis de línea de comandos diferente de la del compilador de DCE IDL.

 

El compilador MIDL cambia [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del servidor.

A partir de la versión 6.0.359 de MIDL, la opción de línea de comandos predeterminada para el  [](-robust.md)compilador MIDL es [**/Oicf**](-oi.md). Para deshabilitar/Robust, especifique la opción [**/no \_ Robust**](-no-robust.md) .

## <a name="the-header-file"></a>El archivo de encabezado

El archivo de encabezado contiene definiciones de todos los tipos de datos y las operaciones declaradas en el archivo IDL. El archivo de encabezado debe estar incluido en todos los módulos de aplicación que llaman a las operaciones definidas, implementan las operaciones definidas o manipulan los tipos definidos.

El compilador MIDL cambia [**/Header**](-header.md) y [**/out**](-out.md) afectan al archivo de encabezado.

 

 




