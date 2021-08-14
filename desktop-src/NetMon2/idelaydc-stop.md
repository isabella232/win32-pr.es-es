---
description: 'Método IDelaydC::Stop: el método Stop detiene la captura actual.'
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: Método IDelaydC::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b5fb6442481574de6732aef1359cf9586b9cdcc1815d9f0b206a1f8a597f1967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366005"
---
# <a name="idelaydcstop-method"></a>IDelaydC::Stop (Método)

El **método Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Puntero a una [estructura STATISTICS que](statistics.md) contiene estadísticas de red, como fotogramas totales y bytes totales capturados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red. Llame [a IDelaydC::Conectar](idelaydc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl> | El NPP no captura datos. Llame [a IDelaydC::Start para](idelaydc-start.md) iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ NO \_ RETRASADO**</dt> </dl>   | El NPP está conectado a la red, pero no con [el método IDelaydC::Conectar.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Cuando **se llama a IDelaydC::Stop,** Monitor de red la captura de datos y cierra el archivo de [*captura*](c.md). (El nombre del archivo de captura se devolvió [cuando se llamó a IDelaydC::Start).](idelaydc-start.md) Ahora puede ver el contenido del archivo de captura.

Cuando detenga e inicie la captura, asegúrese de llamar al método [IDelaydC::Configure](idelaydc-configure.md) cada vez que llame a [IDelaydC::Start](idelaydc-start.md) para reiniciar la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Estadísticas](statistics.md)
</dt> </dl>

 

 




