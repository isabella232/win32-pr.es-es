---
title: Estructura de cadenas
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de copyright o sus marcas comerciales.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menús de estructura de cadenas y otros recursos
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6db2c10e981ae059a46e84e7abfc4d6dfc372fc3c75c76cfc20fd8a8f42735d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776735"
---
# <a name="string-structure"></a>Estructura de cadenas

Representa la organización de los datos en un recurso de versión de archivo. Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de copyright o sus marcas comerciales.

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

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, de esta **estructura String.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tamaño, en palabras, del **miembro Value.**

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo de datos del recurso de versión. Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Cadena Unicode arbitraria. El **miembro szKey** puede ser uno o varios de los valores siguientes. Estos valores son solo directrices.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comentarios**


</dt> <dd>

El **miembro Value** contiene cualquier información adicional que se debe mostrar con fines de diagnóstico. Esta cadena puede ser una longitud arbitraria.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Companyname**


</dt> <dd>

El **miembro** Value identifica la empresa que produjo el archivo. Por ejemplo, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc".

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

El **miembro** Value describe el archivo de forma que se pueda presentar a los usuarios. Esta cadena puede presentarse en un cuadro de lista cuando el usuario elige los archivos que desea instalar. Por ejemplo, "Controlador de teclado para teclados de estilo AT" o "Microsoft Word para Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

El **miembro** Value identifica la versión de este archivo. Por ejemplo, **el valor** podría ser "3.00A" o "5.00.RC2".

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

El **miembro** Value identifica el nombre interno del archivo, si existe alguno. Por ejemplo, esta cadena podría contener el nombre del módulo de un archivo DLL, un nombre de dispositivo virtual para un dispositivo virtual Windows o un nombre de dispositivo para un controlador de dispositivo MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

El **miembro Value** describe todos los avisos de copyright, marcas comerciales y marcas comerciales registradas que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, fechas de copyright, números de marcas comerciales, etc. En inglés, esta cadena debe tener el formato "Copyright Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalMarks**


</dt> <dd>

El **miembro Valor** describe todas las marcas comerciales y marcas comerciales registradas que se aplican al archivo. Esto debe incluir el texto completo de todos los avisos, símbolos legales, números de marcas comerciales, etc. En inglés, esta cadena debe tener el formato "Windows es una marca comercial de Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

El **miembro** Value identifica el nombre original del archivo, sin incluir una ruta de acceso. Esto permite a una aplicación determinar si un usuario ha cambiado el nombre de un archivo. Es posible que este nombre no tenga el formato MS-DOS 8.3 si el archivo es específico de un sistema de archivos que no es FAT.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

El **miembro** Value describe por quién, dónde y por qué se ha creado esta versión privada del archivo. Esta cadena solo debe estar presente si la marca **\_ \_ PRIVATEBUILD** de VS FF está establecida en el **miembro dwFileFlags** de la [**estructura \_ FIXEDFILEINFO de VS.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Por ejemplo, **Value** podría ser "Built by LA \\ onIMOS2".

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**Productname**


</dt> <dd>

El **miembro** Value identifica el nombre del producto con el que se distribuye este archivo. Por ejemplo, esta cadena podría ser "Microsoft Windows".

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**Productversion**


</dt> <dd>

El **miembro** Value identifica la versión del producto con el que se distribuye este archivo. Por ejemplo, **el valor** podría ser "3.00A" o "5.00.RC2".

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

El **miembro** Value describe cómo esta versión del archivo difiere de la versión normal. Esta entrada solo debe estar presente si la marca **\_ \_ SPECIALBUILD** de VS FF está establecida en el **miembro dwFileFlags** de la [**estructura \_ FIXEDFILEINFO de VS.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Por ejemplo, **El** valor podría ser "Compilación privada para la solución de problemas del mouse en equipos M250 y M250E".

</dd> </dl> </dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tantas palabras cero como sea necesario para alinear el **miembro Value** en un límite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Cadena terminada en cero. Consulte la **descripción del miembro szKey** para obtener más información.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura no es una estructura verdadera del lenguaje C porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos con el Kit de desarrollo de software (SDK) de Windows.

Una **estructura String** puede tener un valor **szKey** de, por ejemplo, "CompanyName" y **un valor** de "Microsoft Corporation". Otra **estructura String** con el mismo valor **szKey** podría contener **un valor** de "Microsoft GmbH". Esto puede ocurrir si la segunda estructura **String** se asoció a una estructura [**StringTable**](stringtable.md) cuyo valor **szKey** es 040704b0, es decir, alemán/Unicode.

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

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





