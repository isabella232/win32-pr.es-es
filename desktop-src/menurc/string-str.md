---
title: Estructura de cadena
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de propiedad intelectual o sus marcas comerciales.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menús de estructura de cadena y otros recursos
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695884"
---
# <a name="string-structure"></a>Estructura de cadena

Representa la organización de los datos en un recurso de versión de archivo. Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de propiedad intelectual o sus marcas comerciales.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Longitud, en bytes, de esta estructura de **cadena** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tamaño, en palabras, del miembro de **valor** .

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El tipo de datos del recurso de versión. Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Cadena Unicode arbitraria. El miembro **szKey** puede ser uno o varios de los valores siguientes. Estos valores solo son instrucciones.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Opiniones**


</dt> <dd>

El miembro **Value** contiene cualquier información adicional que se debe mostrar con fines de diagnóstico. Esta cadena puede ser una longitud arbitraria.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Compañía**


</dt> <dd>

El miembro de **valor** identifica la compañía que generó el archivo. Por ejemplo, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

El miembro **Value** describe el archivo de tal forma que se puede presentar a los usuarios. Esta cadena se puede presentar en un cuadro de lista cuando el usuario elige los archivos que se van a instalar. Por ejemplo, "controlador de teclado para teclados de estilo" o "Microsoft Word para Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

El miembro de **valor** identifica la versión de este archivo. Por ejemplo, el **valor** puede ser "3,00 a" o "5,00. RC2".

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

El miembro de **valor** identifica el nombre interno del archivo, si existe alguno. Por ejemplo, esta cadena podría contener el nombre del módulo para un archivo DLL, un nombre de dispositivo virtual para un dispositivo virtual de Windows o un nombre de dispositivo para un controlador de dispositivo de MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

El miembro de **valor** describe todos los avisos de propiedad intelectual, marcas comerciales y marcas registradas que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, fechas de copyright, números de marcas comerciales, etc. En inglés, esta cadena debe tener el formato "Copyright Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**


</dt> <dd>

El miembro **Value** describe todas las marcas comerciales y marcas registradas que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, números de marcas comerciales, etc. En inglés, esta cadena debe tener el formato "Windows es una marca comercial de Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

El miembro de **valor** identifica el nombre original del archivo, sin incluir una ruta de acceso. Esto permite que una aplicación determine si un usuario ha cambiado el nombre de un archivo. Este nombre no puede ser MS-DOS 8,3-Format si el archivo es específico de un sistema de archivos que no es FAT.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

El miembro de **valor** describe quién, dónde y por qué se compiló esta versión privada del archivo. Esta cadena solo debe estar presente si la marca **vs \_ FF \_ PRIVATEBUILD** se establece en el miembro **dwFileFlags** de la estructura [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Por ejemplo, el **valor** podría ser "compilado por Oscar en \\ OSCAR2".

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**NombreDeProducto**


</dt> <dd>

El miembro de **valor** identifica el nombre del producto con el que se distribuye este archivo. Por ejemplo, esta cadena podría ser "Microsoft Windows".

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**


</dt> <dd>

El miembro de **valor** identifica la versión del producto con el que se distribuye este archivo. Por ejemplo, el **valor** puede ser "3,00 a" o "5,00. RC2".

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

El miembro **Value** describe el modo en que esta versión del archivo difiere de la versión normal. Esta entrada solo debe estar presente si la marca **vs \_ FF \_ SPECIALBUILD** se establece en el miembro **dwFileFlags** de la estructura [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Por ejemplo, el **valor** podría ser "compilación privada para la solución de problemas del mouse en los equipos M250 y M250E".

</dd> </dl> </dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palabras como sea necesario para alinear el miembro de **valor** en un límite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Cadena terminada en cero. Vea la descripción del miembro **szKey** para obtener más información.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.

Una estructura de **cadena** puede tener un valor **szKey** de, por ejemplo, "CompanyName" y un **valor** de "Microsoft Corporation". Otra estructura de **cadena** con el mismo valor de **szKey** podría contener un **valor** de "Microsoft GmbH". Esto puede ocurrir si la segunda estructura de **cadena** estaba asociada a una estructura [**StringTable**](stringtable.md) cuyo valor de **szKey** es 040704b0, alemán o Unicode.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ versionInfo**](vs-versioninfo.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





