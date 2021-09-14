---
title: Serialización de tipos de datos OLE
description: Serialización de tipos de datos de Automation y OLE.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL y COM MIDL, serializar tipos de datos OLE
- serialización de MIDL
- DATOS OLE MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159506"
---
# <a name="marshaling-ole-data-types"></a>Serialización de tipos de datos OLE

Para facilitar el uso de determinados tipos de datos de Automation y OLE, así como algunos identificadores del sistema que se usan con frecuencia en COM, las definiciones de tipos para estos tipos de datos y sus funciones auxiliares relacionadas están disponibles mediante la importación de archivos IDL de Windows y la vinculación a los archivos DLL de OLE y Automation. Estos archivos se instalan automáticamente en el sistema.

-   Para usar el tipo de datos [**BSTR**](/previous-versions/windows/desktop/automat/bstr) en llamadas a procedimientos remotos, importe el archivo wtypes.idl en el archivo de definición de interfaz (IDL) y vincule a Oleaut32.lib al compilar la aplicación distribuida. Esto permitirá que los códigos auxiliares usen las funciones auxiliares listas para usar **BSTR \_ UserSize**, **BSTR \_ UserMarshal,** **BSTR \_ UserUnmarshal** y **BSTR \_ UserFree.**
-   Para usar otros tipos de datos de Automation, como [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) y [**SAFEARRAY,**](/windows/win32/api/oaidl/ns-oaidl-safearray)o los tipos que usan esos tipos (por ejemplo, [**DIS DISYRAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) y [**EXCEPINFO),**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)importe el archivo objidl.idl en el archivo IDL y vincule a oleaut32.lib en tiempo de compilación. Esto le permitirá usar las rutinas auxiliares adecuadas.
-   Para usar tipos de datos OLE (como CLIPFORMAT, SNB, STGMEDIUM, ASYNC STGMEDIUM) o identificadores del sistema \_ (como HMETAFILE \_ CLIP, HEHIBMETAFILE, HMETAFILE, HBITMAP, HPALETTE y HGLOBAL), importe el archivo objidl.idl en el archivo de definición de interfaz y vincule al archivo ole32.lib en tiempo de compilación.
-   Los siguientes identificadores OLE también se definen con el atributo wire **\[ \_ marshal, \]** pero solo como identificadores dentro de un equipo, ya que no se pueden usar en llamadas a procedimientos remotos a otros equipos en este momento: HWND, HMENU, HACCEL, HDC, HFONT, HICON, HBRUSH. Importe el archivo objidl.idl en el archivo IDL y vincule a ole32.lib en tiempo de compilación para usar estos identificadores en la comunicación entre procesos en un solo equipo.

Para obtener más información, vea The [wire \_ marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute), The type [ \_ UserSize Function](/windows/desktop/Rpc/the-type-usersize-function), The type [ \_ UserMarshal Function](/windows/desktop/Rpc/the-type-usermarshal-function), The type [ \_ UserUnmarshal Function](/windows/desktop/Rpc/the-type-userunmarshal-function), The type [ \_ UserFree Function](/windows/desktop/Rpc/the-type-userfree-function), and [Targeting Stubs for Specific 32-bit or 64-bit Platforms](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 