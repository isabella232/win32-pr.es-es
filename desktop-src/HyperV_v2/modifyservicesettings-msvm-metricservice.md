---
description: Modifica los datos de configuración para el servicio.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Método ModifyServiceSettings de la clase Msvm_MetricService
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
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810316"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Método ModifyServiceSettings de la \_ clase MetricService de MSVM

Modifica los datos de configuración para el servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SettingData* \[ de\]
</dt> <dd>

Contiene una instancia incrustada de la clase [**MSVM \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contiene los datos de configuración modificados para el servicio.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                                | Descripción                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                    | Correcto.<br/>                                |
| <dl> <dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt> </dl> | Parámetros de método comprobados, trabajo iniciado.<br/> |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                 | Failed.<br/>                                 |
| <dl> <dt>**Acceso Denegado**</dt> <dt>32769</dt> </dl>                          | Acceso denegado.<br/>                          |
| <dl> <dt>**No compatible**</dt> <dt>32770</dt> </dl>                          | No se admite.<br/>                          |
| <dl> El <dt>**Estado es desconocido**</dt> <dt>32771</dt> </dl>                      | Se desconoce el estado de conexión.<br/>                      |
| <dl> <dt>**Tiempo de espera**</dt> <dt>32772</dt> </dl>                                | Tiempo de espera.<br/>                               |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                      | Parámetro no válido.<br/>                      |
| <dl> El <dt>**sistema está en uso**</dt> <dt>32774</dt> </dl>                       | El sistema está en uso.<br/>                       |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>       | Estado no válido para esta operación.<br/>       |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                    | Tipo de datos incorrecto.<br/>                    |
| <dl> El <dt>**sistema no está disponible**</dt> <dt>32777</dt> </dl>                | El sistema no está disponible.<br/>                |
| <dl> <dt>**Memoria**</dt> insuficiente <dt>32778</dt> </dl>                          | Memoria insuficiente<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

