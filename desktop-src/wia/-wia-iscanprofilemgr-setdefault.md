---
description: Establece el perfil de examen especificado como perfil predeterminado.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: Método IScanProfileMgr::SetDefault (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: fd7b46241e967e02083c344aa7f3f77a773c72b02ff74b225910788d498fe252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965801"
---
# <a name="iscanprofilemgrsetdefault-method"></a>IScanProfileMgr::SetDefault (método)

Establece el perfil de examen especificado como perfil predeterminado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pScanProfile* \[ En\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\***

Puntero al perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Use el **método IScanProfileMgr::SetDefault** para agregar un elemento al perfil o para quitar ese elemento del perfil `<Default>` predeterminado anterior del dispositivo.

Use el [**método ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) para cambiar el perfil predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




