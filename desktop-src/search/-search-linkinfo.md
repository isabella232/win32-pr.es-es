---
description: Almacena información sobre los tipos de vínculo y lo usa la interfaz IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Estructura LINKINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275267"
---
# <a name="linkinfo-structure"></a>Estructura LINKINFO

\[**LINKINFO** y [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admiten en Windows XP y Windows Server 2003, y ya no deben usarse.\]

Almacena información sobre los tipos de vínculo y lo usa la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**type**
</dt> <dd>

Tipo: **[ **LINKTYPE**](-search-linktype.md)**

</dd> <dd>

El tipo de vínculo especificado al rastrear o indizar indicado por una constante [**LINKTYPE**](-search-linktype.md) .

</dd> <dt>

**bstrContentType**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valor **BSTR** que especifica el tipo de contenido.

</dd> <dt>

**bstrEncoding**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Atributo EncodingStyle especificado en el archivo de lenguaje de descripción de servicios web (WSDL).

</dd> <dt>

**bstrFileExt**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valor **BSTR** que especifica la extensión de nombre de archivo.

</dd> <dt>

**varData**
</dt> <dd>

Tipo: **variante**

</dd> <dd>

Variante que especifica el valor de la variable.

</dd> <dt>

**dwRelatedParts**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

**DWORD** que especifica las partes relacionadas.

</dd> <dt>

**bstrRelatedCid**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valor **BSTR** que especifica una propiedad Cid, una cadena decimal con signo no rellenada.

</dd> <dt>

**lCodePage**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Página de códigos que se va a usar para codificar la cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la estructura **LINKINFO** y las siguientes API: los métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) y [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) , y la enumeración [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>          |



 

 




