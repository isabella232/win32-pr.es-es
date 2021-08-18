---
description: Almacena información sobre los tipos de vínculo y la interfaz IItemPreviewerExt la usa.
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
ms.openlocfilehash: 97c106a5a819ac1068501c77555f3eae238c935e2262894c6c250dfc6782188f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863948"
---
# <a name="linkinfo-structure"></a>Estructura LINKINFO

\[**LINKINFO** e [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admiten en Windows XP y Windows Server 2003 y ya no se deben usar.\]

Almacena información sobre los tipos de vínculo y la [**interfaz IItemPreviewerExt**](-search-iitempreviewerext.md) la usa.

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

Tipo de vínculo especificado al rastrear o indexar indicado por una [**constante LINKTYPE.**](-search-linktype.md)

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

Atributo EncodingStyle especificado en el archivo WSDL (Lenguaje de descripción de servicios Web).

</dd> <dt>

**bstrFileExt**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valor **BSTR** que especifica la extensión de nombre de archivo.

</dd> <dt>

**varData**
</dt> <dd>

Tipo: **VARIANT**

</dd> <dd>

Variante que especifica el valor de variable.

</dd> <dt>

**dwRelatedParts**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

DWORD **que** especifica las partes relacionadas.

</dd> <dt>

**bstrRelatedCid**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Valor **BSTR** que especifica una propiedad Cid, una cadena decimal no agregada y con signo.

</dd> <dt>

**lCodePage**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Página de códigos que se usará para codificar la cadena.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la estructura **LINKINFO** y las siguientes API: los métodos [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



 

 




