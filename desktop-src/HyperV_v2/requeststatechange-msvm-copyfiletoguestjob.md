---
description: Cambia el estado del trabajo.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Msvm_CopyFileToGuestJob:: RequestStateChange (método)'
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
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687842"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>MSVM \_ CopyFileToGuestJob:: RequestStateChange (método)

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

*RequestedState* \[ de\]
</dt> <dd>

El nuevo estado. Estos son los valores posibles:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)


</dt> <dd>

Cambia el estado a "en ejecución".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Detiene el trabajo temporalmente. Después, el cliente puede reiniciar el trabajo con "Start". Es posible que el cliente pueda entrar en el estado "servicio" mientras está suspendido (es específico del trabajo).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)


</dt> <dd>

Detiene el trabajo limpiamente, guarda los datos, conserva el estado y cerrando todos los procesos subyacentes de forma ordenada.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)


</dt> <dd>

Coloca el trabajo en un estado de servicio específico del proveedor. Es posible que el cliente reinicie el trabajo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ de\]
</dt> <dd>

Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado. El formato de intervalo debe usarse para especificar el período de tiempo de espera. Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición. Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (**no se admite el uso del parámetro timeout**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                               | Descripción                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                   | Correcto.<br/>                                                                |
| <dl> <dt>**No se admite el uso del parámetro Timeout**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Acceso Denegado**</dt> <dt>32769</dt> </dl>                         | Acceso denegado.<br/>                                                          |
| <dl> <dt>**No compatible**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> El <dt>**Estado es desconocido**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Tiempo de espera**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> El <dt>**sistema está en uso**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>      | No se admite el valor especificado en el parámetro *RequestedState* .<br/> |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> El <dt>**sistema no está disponible**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Memoria**</dt> insuficiente <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\\\Virtualización de raíz \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




