---
title: Método SynchronizePublishingData de la Win32_RDMSManagementData clase
description: Sincroniza el conjunto de datos de publicación especificado para Escritorio remoto Management Services (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Método SynchronizePublishingData Servicios de Escritorio remoto
- Método SynchronizePublishingData Servicios de Escritorio remoto , Win32_RDMSManagementData clase
- Win32_RDMSManagementData clase Servicios de Escritorio remoto método , SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5cadc3581419fa758775a48ba0190300a176364dcf0aad5a8a3ed77fa1db8bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000335"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Método SynchronizePublishingData de la clase \_ RDMSManagementData de Win32

Sincroniza el conjunto de datos de publicación especificado para Escritorio remoto Management Services (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Contexto* \[ En\]
</dt> <dd>

Información de contexto de los datos de publicación que se sincronizarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RdMSManagementData de Win32 \_**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





