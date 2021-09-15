---
description: 'Método IESP::Start: el método Start inicia una captura.'
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: Método IESP::Start (Netmon.h)
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
ms.openlocfilehash: 6dd0d1159132e594b6d48ea6799da5846eeb626e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476717"
---
# <a name="iespstart-method"></a>IESP::Start (método)

El **método Start** inicia una captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileName* \[ out\]
</dt> <dd>

Puntero al nombre del archivo [*de captura utilizado*](c.md) para almacenar los datos de red. Asegúrese de almacenar en caché este nombre de archivo si es necesario para futuras referencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt> </dl> | La captura está en pausa y debe detenerse antes de poder reiniciarse. Llame [a IESP::Stop](iesp-stop.md) para detener la captura.<br/> |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>       | La captura ya se ha iniciado.<br/>                                                                                             |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>  | El NPP no está conectado a la red. Llame [a IESP::Conectar](iesp-connect.md) para conectar el NPP a la red.<br/>          |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>        | El NPP está conectado a la red, pero no con el [método IESP::Conectar.](iesp-connect.md)<br/>                              |



 

## <a name="remarks"></a>Observaciones

La ubicación del [*archivo de captura*](c.md) se especifica en el registro Windows, pero puede usar Monitor de red para cambiar la ubicación del directorio.

Al reiniciar la captura mediante los métodos IESP::Start e [IESP::Stop,](iesp-stop.md) debe llamar al método [IESP::Configure](iesp-configure.md) para volver a configurar la conexión cada vez que llame a IESP::Start para reiniciar la captura de datos. Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.

> [!Note]  
> También puede iniciar y detener la captura mediante los métodos [IESP::P ause](iesp-pause.md) [e IESP::Resume.](iesp-resume.md) Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Configure](iesp-configure.md)
</dt> <dt>

[IESP::Conectar](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP::Resume](iesp-resume.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 




