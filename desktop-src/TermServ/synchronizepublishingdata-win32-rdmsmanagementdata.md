---
title: Método SynchronizePublishingData de la clase Win32_RDMSManagementData
description: Sincroniza el conjunto especificado de datos de publicación para Escritorio remoto Management Services (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Método SynchronizePublishingData Servicios de Escritorio remoto
- Método SynchronizePublishingData Servicios de Escritorio remoto, clase Win32_RDMSManagementData
- Win32_RDMSManagementData de clase Servicios de Escritorio remoto, método SynchronizePublishingData
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
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422262"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Método SynchronizePublishingData de la \_ clase RDMSManagementData de Win32

Sincroniza el conjunto especificado de datos de publicación para Escritorio remoto Management Services (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Contexto* \[ de de\]
</dt> <dd>

Información de contexto de los datos de publicación que se van a sincronizar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSManagementData**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





