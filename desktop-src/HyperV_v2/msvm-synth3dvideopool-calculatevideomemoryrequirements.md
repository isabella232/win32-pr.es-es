---
description: Calcula la cantidad de memoria de vídeo necesaria para una máquina virtual de RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Método CalculateVideoMemoryRequirements de la clase Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154592"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Método CalculateVideoMemoryRequirements de la \_ clase Synth3dVideoPool de MSVM

Calcula la cantidad de memoria de vídeo necesaria para una máquina virtual de RemoteFX.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*monitorResolution* \[ de\]
</dt> <dd>

La resolución máxima del monitor de la máquina virtual. Debe ser uno de los valores siguientes.



| Value                                                                        | Significado                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La resolución máxima es 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | La resolución máxima es 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | La resolución máxima es 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | La resolución máxima es 1920 1200.<br/> |



 

</dd> <dt>

*numberOfMonitors* \[ de\]
</dt> <dd>

Número máximo de monitores para la máquina virtual. El número mínimo de monitores es uno y el máximo depende de la resolución de pantalla máxima. En la tabla siguiente se define el número máximo de monitores permitido para diferentes resoluciones.



| Solución             | Monitores máximos |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[ enuncia\]
</dt> <dd>

Recibe la cantidad necesaria de memoria de vídeo, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de estado, que puede ser uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                                | Descripción                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                    | Ejecutado.<br/>                                |
| <dl> <dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt> </dl> | Trabajo iniciado.<br/>                               |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                 | Failed.<br/>                                    |
| <dl> <dt>**Acceso Denegado**</dt> <dt>32769</dt> </dl>                          | Acceso denegado.<br/>                             |
| <dl> <dt>**No compatible**</dt> <dt>32770</dt> </dl>                          | No se admite.<br/>                             |
| <dl> El <dt>**Estado es desconocido**</dt> <dt>32771</dt> </dl>                      | Se desconoce el estado de conexión.<br/>                         |
| <dl> <dt>**Tiempo de espera**</dt> <dt>32772</dt> </dl>                                | Tiempo de espera.<br/>                                   |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                      | Un parámetro no es válido.<br/>                  |
| <dl> El <dt>**sistema está en uso**</dt> <dt>32774</dt> </dl>                      | El sistema está en uso.<br/>                          |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>       | El estado no es válido para esta operación.<br/> |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                    | Tipo de datos incorrecto.<br/>                       |
| <dl> El <dt>**sistema no está disponible**</dt> <dt>32777</dt> </dl>                | El sistema no está disponible.<br/>                   |
| <dl> <dt>**Memoria**</dt> insuficiente <dt>32778</dt> </dl>                          | Memoria insuficiente<br/>                             |



 

## <a name="remarks"></a>Observaciones

Normalmente, se llama a este método en el sistema host para determinar si el host tiene suficiente memoria de vídeo disponible para hospedar una máquina virtual de RemoteFX. Para ello, compare la cantidad de memoria de vídeo calculada por este método con la propiedad [**MSVM \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) para determinar si el equipo host tiene suficiente memoria de vídeo disponible. Puede usar esta información para determinar si una máquina virtual se puede migrar al sistema host.

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

[**MSVM \_ PhysicalGPUInfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**MSVM \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




