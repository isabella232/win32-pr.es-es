---
description: Vuelve a enumerar todos los perfiles de digitalización en el sistema.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'IScanProfileMgr:: Refresh (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001301"
---
# <a name="iscanprofilemgrrefresh-method"></a>IScanProfileMgr:: Refresh (método)

Vuelve a enumerar todos los perfiles de digitalización en el sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Refresh();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Use este método cuando más de un objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pueda estar creando o eliminando perfiles al mismo tiempo.

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

 

 




