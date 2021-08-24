---
description: 'Método ModifyServiceSettings de la Msvm_MetricService : modifica los datos de configuración del servicio.'
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Método ModifyServiceSettings de la Msvm_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 51af98d230433687d9a16cb3ab858fd746b7ff1ca4e17eaf0b36cce16e92c875
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693915"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Método ModifyServiceSettings de la clase MetricService de Msvm \_

Modifica los datos de configuración del servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SettingData* \[ En\]
</dt> <dd>

Contiene una instancia incrustada de la [**clase \_ Msvm MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contiene los datos de configuración modificados para el servicio.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                                | Descripción                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                    | Correcto.<br/>                                |
| <dl> <dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt> </dl> | Parámetros de método activados, trabajo iniciado.<br/> |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                 | Failed.<br/>                                 |
| <dl> <dt>**Acceso denegado**</dt> <dt>32769</dt> </dl>                          | Acceso denegado:<br/>                          |
| <dl> <dt>**No compatible**</dt> <dt>con 32770</dt> </dl>                          | No compatible.<br/>                          |
| <dl> <dt>**El estado es desconocido**</dt> <dt>32771</dt> </dl>                      | Se desconoce el estado de conexión.<br/>                      |
| <dl> <dt>**Tiempo de**</dt> <dt>espera 32772</dt> </dl>                                | Tiempo de espera.<br/>                               |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                      | Parámetro no válido.<br/>                      |
| <dl> <dt>**El sistema está en uso**</dt> <dt>32774</dt> </dl>                       | El sistema está en uso.<br/>                       |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>       | Estado no válido para esta operación.<br/>       |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                    | Tipo de datos incorrecto.<br/>                    |
| <dl> <dt>**El sistema no está disponible**</dt> <dt>32777</dt> </dl>                | El sistema no está disponible.<br/>                |
| <dl> <dt>**Memoria sin memoria**</dt> <dt>32778</dt> </dl>                          | Memoria insuficiente<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

