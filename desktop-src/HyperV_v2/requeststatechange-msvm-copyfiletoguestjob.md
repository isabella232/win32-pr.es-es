---
description: Cambia el estado del trabajo.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: Msvm_CopyFileToGuestJob::RequestStateChange (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09fdc3a1ee7d0f8942e1e02c5d18f20c42f74db2e65ae065132f164b199ee861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014343"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>Método \_ CopyFileToGuestJob::RequestStateChange de Msvm

Cambia el estado del trabajo.

## <a name="syntax"></a>Sintaxis


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedState* \[ En\]
</dt> <dd>

El nuevo estado. Estos son los valores posibles:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)


</dt> <dd>

Cambia el estado a "En ejecución".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Detiene temporalmente el trabajo. A continuación, el cliente puede reiniciar el trabajo con "Iniciar". Es posible que el cliente escriba el estado "Servicio" mientras está suspendido (esto es específico del trabajo).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)


</dt> <dd>

Detiene el trabajo de forma limpia, guardando datos, conservando el estado y cerrando todos los procesos subyacentes de forma ordenada.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Finaliza el trabajo inmediatamente sin necesidad de guardar datos o conservar el estado.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)


</dt> <dd>

Coloca el trabajo en un estado de servicio específico del proveedor. Es posible que el cliente reinicie el trabajo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ En\]
</dt> <dd>

Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado. El formato de intervalo debe usarse para especificar el período de tiempo de espera. Un valor de 0 o **Null** indica que el cliente no tiene ningún requisito de tiempo para la transición. Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 (**Use Of Timeout Parameter Not Supported**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                               | Descripción                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                   | Correcto.<br/>                                                                |
| <dl> <dt>**No se admite el uso del parámetro timeout**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Acceso denegado**</dt> <dt>32769</dt> </dl>                         | Acceso denegado:<br/>                                                          |
| <dl> <dt>**No compatible**</dt> <dt>con 32770</dt> </dl>                         |                                                                                    |
| <dl> <dt>**El estado es desconocido**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Tiempo de**</dt> <dt>espera 32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> <dt>**El sistema está en uso**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>      | No se admite el valor especificado *en el parámetro RequestedState.*<br/> |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> <dt>**El sistema no está disponible**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Memoria sin memoria**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




