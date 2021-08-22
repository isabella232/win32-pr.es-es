---
description: Calcula la cantidad de memoria de vídeo necesaria para una RemoteFX virtual.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Método CalculateVideoMemoryRequirements de la Msvm_Synth3dVideoPool clase
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
ms.openlocfilehash: 2fd1485cdd4e96155db6540a5f07344add5f413514a92c420fcac78a008e7aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950084"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Método CalculateVideoMemoryRequirements de la clase \_ Msvm Synth3dVideoPool

Calcula la cantidad de memoria de vídeo necesaria para una RemoteFX virtual.

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

*monitorResolution* \[ En\]
</dt> <dd>

Resolución máxima del monitor para la máquina virtual. Debe ser uno de los siguientes valores.



| Value                                                                        | Significado                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La resolución máxima es 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | La resolución máxima es 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | La resolución máxima es 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | La resolución máxima es 1920 1200.<br/> |



 

</dd> <dt>

*numberOfMonitors* \[ En\]
</dt> <dd>

Número máximo de monitores para la máquina virtual. El número mínimo de monitores es uno y el máximo depende de la resolución de pantalla máxima. En la tabla siguiente se define el número máximo de monitores permitidos para diferentes resoluciones.



| Resolución             | Monitores máximos |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[ out\]
</dt> <dd>

Recibe la cantidad necesaria de memoria de vídeo, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de estado, que puede ser uno de los siguientes valores.



| Código o valor devuelto                                                                                                                                                                | Descripción                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                    | Exitoso.<br/>                                |
| <dl> <dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt> </dl> | Trabajo iniciado.<br/>                               |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                 | Failed.<br/>                                    |
| <dl> <dt>**Acceso denegado**</dt> <dt>32769</dt> </dl>                          | Acceso denegado:<br/>                             |
| <dl> <dt>**No compatible**</dt> <dt>con 32770</dt> </dl>                          | No compatible.<br/>                             |
| <dl> <dt>**El estado es desconocido**</dt> <dt>32771</dt> </dl>                      | Se desconoce el estado de conexión.<br/>                         |
| <dl> <dt>**Tiempo de**</dt> <dt>espera 32772</dt> </dl>                                | Tiempo de espera.<br/>                                   |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                      | Un parámetro no es válido.<br/>                  |
| <dl> <dt>**El sistema se usa**</dt> <dt>en la 32774</dt> </dl>                      | El sistema está en uso.<br/>                          |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>       | El estado no es válido para esta operación.<br/> |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                    | Tipo de datos incorrecto.<br/>                       |
| <dl> <dt>**El sistema no está disponible**</dt> <dt>32777</dt> </dl>                | El sistema no está disponible.<br/>                   |
| <dl> <dt>**Memoria sin memoria**</dt> <dt>32778</dt> </dl>                          | Memoria insuficiente<br/>                             |



 

## <a name="remarks"></a>Comentarios

Normalmente, se llama a este método en el sistema host para determinar si el host tiene suficiente memoria de vídeo disponible para hospedar una RemoteFX virtual. Para ello, compare la cantidad de memoria de vídeo calculada por este método con la propiedad [**\_ Msvm PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) para determinar si la máquina host tiene suficiente memoria de vídeo disponible. Puede usar esta información para determinar si una máquina virtual se puede mover al sistema host.

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

[**Msvm \_ PhysicalGPUInfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**Msvm \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




