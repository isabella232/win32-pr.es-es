---
title: Método GetStringProperty de la clase Win32_RDSHCollection
description: Recupera un valor de propiedad de cadena de un \_ objeto RDSHCollection de Win32.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Servicios de Escritorio remoto
- Método GetStringProperty Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996081"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a>Método GetStringProperty de la \_ clase RDSHCollection de Win32

Recupera un valor de propiedad de cadena de un objeto [**\_ RDSHCollection de Win32**](win32-rdshcollection.md) .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ de de\]
</dt> <dd>

Clave que identifica la propiedad que se va a recuperar.

</dd> <dt>

*Valor* \[ de enuncia\]
</dt> <dd>

Recibe el valor de la propiedad recuperada.

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

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





