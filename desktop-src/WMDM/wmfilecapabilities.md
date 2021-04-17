---
title: Estructura WMFILECAPABILITIES
description: La estructura WMFILECAPABILITIES describe el tipo MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Estructura WMFILECAPABILITIES Administrador de dispositivos Windows Media
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698640"
---
# <a name="wmfilecapabilities-structure"></a>Estructura WMFILECAPABILITIES

La estructura **WMFILECAPABILITIES** describe el tipo MIME.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pwszMimeType**
</dt> <dd>

Tipo MIME.

</dd> <dt>

**dwReserved**
</dt> <dd>

**DWORD** reservado para uso futuro. Se establece en cero (0).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





