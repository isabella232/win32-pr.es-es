---
description: Define formas de asignar a un identificador de clase.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Enumeración TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: 15e7ecdc06495c0fa68b2949ae159bbc76b8cababd2b8703d3ebbdebb874399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075759"
---
# <a name="tyspec-enumeration"></a>Enumeración TYSPEC

Define formas de asignar a un identificador de clase.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**CLSID de TYSPEC \_**
</dt> <dd>

A CLSID.

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**
</dt> <dd>

Extensión de nombre de archivo. Este valor no se admite actualmente.

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC \_ MIMETYPE**
</dt> <dd>

Tipo MIME. Este valor no se admite actualmente.

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**NOMBRE DE ARCHIVO DE TYSPEC \_**
</dt> <dd>

Un nombre de archivo. Este valor no se admite actualmente.

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**PROGID de TYSPEC \_**
</dt> <dd>

A PROGID. Este valor no se admite actualmente.

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PACKAGENAME**
</dt> <dd>

Nombre del paquete. Este valor no se admite actualmente.

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**OBJECTID de TYSPEC \_**
</dt> <dd>

Un identificador de objeto. Este valor no se admite actualmente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **unión uCLSSPEC** se define de la siguiente manera:

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Wtypes.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CoInstall**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
