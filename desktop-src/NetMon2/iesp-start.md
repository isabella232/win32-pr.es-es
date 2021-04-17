---
description: El método start inicia una captura.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP:: Start (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687322"
---
# <a name="iespstart-method"></a>IESP:: Start (método)

El método **Start** inicia una captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileName* \[ enuncia\]
</dt> <dd>

Puntero al nombre del archivo de [*captura*](c.md) que se usa para almacenar los datos de red. Asegúrese de almacenar en caché este nombre de archivo si es necesario para futuras referencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl> | La captura se pausa y debe detenerse antes de que se pueda reiniciar. Llame a [iesp:: Stop](iesp-stop.md) para detener la captura.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>       | La captura ya se ha iniciado.<br/>                                                                                             |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>  | NPP no está conectado a la red. Llame a [iesp:: Connect](iesp-connect.md) para conectar el NPP a la red.<br/>          |
| <dl> <dt>**NMERR \_ no \_ ESP**</dt> </dl>        | NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .<br/>                              |



 

## <a name="remarks"></a>Observaciones

La ubicación del [*archivo de captura*](c.md) se especifica en el registro de Windows, pero puede usar Monitor de red para cambiar la ubicación del directorio.

Cuando reinicie la captura mediante los métodos IESP:: Start y [iesp:: Stop](iesp-stop.md) , debe llamar al método [iesp:: configure](iesp-configure.md) para volver a configurar la conexión cada vez que llame a iesp:: Start para reiniciar la captura de datos. Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.

> [!Note]  
> También puede iniciar y detener la captura mediante los métodos [iesp::P ause](iesp-pause.md) y [iesp:: resume](iesp-resume.md) . Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP:: configure](iesp-configure.md)
</dt> <dt>

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP:: resume](iesp-resume.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> </dl>

 

 




