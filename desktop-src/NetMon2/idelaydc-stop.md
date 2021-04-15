---
description: El método Stop detiene la captura actual.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'IDelaydC:: STOP (método) (Netmon. h)'
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
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496984"
---
# <a name="idelaydcstop-method"></a>IDelaydC:: STOP (método)

El método **Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [estadísticas](statistics.md) que contiene estadísticas de red como el total de tramas y el total de bytes capturados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl> | NPP no está conectado a la red. Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl> | NPP no está capturando datos. Llame a [IDelaydC:: Start](idelaydc-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no \_ retrasado**</dt> </dl>   | NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Cuando se llama a **IDelaydC:: Stop** , monitor de red detiene la captura de datos y cierra el [*archivo de captura*](c.md). (El nombre del archivo de captura se devolvió cuando se llamó a [IDelaydC:: Start](idelaydc-start.md) ). Ahora puede examinar el contenido del archivo de captura.

Al detener e iniciar la captura, asegúrese de llamar al método [IDelaydC:: configure](idelaydc-configure.md) cada vez que llame a [IDelaydC:: Start](idelaydc-start.md) para reiniciar la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC:: configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[¡](statistics.md)
</dt> </dl>

 

 




