---
title: Serialización de tipos de datos OLE
description: Serialización de tipos de datos OLE y Automation.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL y COM MIDL, serialización de tipos de datos OLE
- calcular las referencias de MIDL
- OLE Data MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790017"
---
# <a name="marshaling-ole-data-types"></a>Serialización de tipos de datos OLE

Para facilitar el uso de determinados tipos de datos OLE y de automatización, así como algunos de los identificadores del sistema que se usan con frecuencia en COM, las definiciones de tipo de estos tipos de datos y sus funciones auxiliares relacionadas están disponibles mediante la importación de archivos IDL de Windows y la vinculación a los archivos DLL de OLE y Automation. Estos archivos se instalan automáticamente en el sistema.

-   Para usar el tipo de datos [**BSTR**](/previous-versions/windows/desktop/automat/bstr) en llamadas a procedimientos remotos, importe el archivo Wtypes. idl en el archivo de definición de interfaz (IDL) y vincúlelo a oleaut32. lib al compilar la aplicación distribuida. Esto permitirá que el código auxiliar use las funciones auxiliares preparadas **de \_ usuario BSTR**, **BSTR \_ UserMarshal**, **BSTR \_ UserUnmarshal** y **BSTR \_ UserFree**.
-   Para usar otros tipos de datos de automatización, como [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) y [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray), o tipos que usan esos tipos (por ejemplo, [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) y [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)), importe el archivo objidl. idl en el archivo IDL y vincule a oleaut32. lib en tiempo de compilación. Esto le permitirá usar las rutinas auxiliares adecuadas.
-   Para usar tipos de datos OLE (como CLIPFORMAT, SNB, STGMEDIUM, ASYNC \_ STGMEDIUM) o identificadores del sistema (como HMETAFILE \_ PICT, HENHMETAFILE, HMETAFILE, hBitmap, HPALETTE y hglobal), importe el archivo objidl. idl en el archivo de definición de la interfaz y vincúlelo a ole32. lib en tiempo de compilación.
-   Los siguientes identificadores OLE también se definen con el atributo de **\[ \_ serialización \] de conexión** , pero solo como identificadores dentro de un equipo, ya que no se pueden usar en llamadas a procedimientos remotos a otros equipos en este momento: HWND, HMENU, HACCEL, HDC, HFONT, HICON, hbrush. Importe el archivo objidl. idl en el archivo IDL y vincúlelo a ole32. lib en el momento de la compilación para utilizar estos identificadores en la comunicación entre procesos en un solo equipo.

Para obtener más información, vea [el \_ atributo de serialización](/windows/desktop/Rpc/the-wire-marshal-attribute)de la conexión, [la función de tipo de \_ usuario](/windows/desktop/Rpc/the-type-usersize-function), la función type [ \_ UserMarshal](/windows/desktop/Rpc/the-type-usermarshal-function), la función type [ \_ UserUnmarshal](/windows/desktop/Rpc/the-type-userunmarshal-function), [la \_ función type UserFree y el](/windows/desktop/Rpc/the-type-userfree-function) [código auxiliar de destino para plataformas específicas de 32 bits o 64](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md)bits.

 

 