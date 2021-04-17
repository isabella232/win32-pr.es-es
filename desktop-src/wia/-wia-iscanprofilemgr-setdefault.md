---
description: Establece el perfil de digitalización especificado como perfil predeterminado.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'IScanProfileMgr:: SetDefault (método) (Scanprofilemgr. h)'
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
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667489"
---
# <a name="iscanprofilemgrsetdefault-method"></a>IScanProfileMgr:: SetDefault (método)

Establece el perfil de digitalización especificado como perfil predeterminado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pScanProfile* \[ de\]
</dt> <dd>

Tipo: **[**IScanProfile**](-wia-iscanprofile.md) \** _

Puntero al perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Use el método **IScanProfileMgr:: SetDefault** para agregar un `<Default>` elemento al perfil o para quitar ese elemento del perfil predeterminado anterior del dispositivo.

Use el método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) para cambiar el perfil predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




