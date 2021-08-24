---
description: 'Método IDelaydC::Start: el método Start inicia una captura.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: Método IDelaydC::Start (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 750a33241358aee924ed3f91491185117a77a548a87bdfc5514d59fe4798a42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365870"
---
# <a name="idelaydcstart-method"></a>IDelaydC::Start (método)

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



| Código devuelto                                                                                           | Descripción                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt> </dl> | La captura está en estado en pausa y debe detenerse antes de poder reiniciarse. Llame [**a IDelaydC::Stop**](idelaydc-stop.md) para detener la captura. Para obtener más información, vea la sección Comentarios de este tema.<br/> |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>       | La captura ya se ha iniciado.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>  | El NPP no está conectado a la red. Llame [**a IDelaydC::Conectar**](idelaydc-connect.md) para conectarse a la red.<br/>                                                                                          |
| <dl> <dt>**NMERR \_ NO \_ RETRASADA**</dt> </dl>    | El NPP está conectado a la red, pero no con [**el método IDelaydC::Conectar.**](idelaydc-connect.md)<br/>                                                                                                      |



 

## <a name="remarks"></a>Comentarios

La ubicación del [*archivo de captura*](c.md) se especifica en el registro de Windows, pero puede usar Monitor de red para cambiar la ubicación del archivo.

Para reiniciar la captura mediante **IDelaydC::Start** e [**IDelaydC::Stop**](idelaydc-stop.md), debe llamar al método [**IDelaydC::Configure**](idelaydc-configure.md) para volver a configurar la conexión cada vez que llame al método **IDelaydC::Start** para reiniciar la captura de datos. Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.

> [!Note]  
> También puede iniciar y detener la captura mediante los métodos [**IDelaydC::P ause**](idelaydc-pause.md) [**e IDelaydC::Resume.**](idelaydc-resume.md) Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.

 

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

[**IDelaydC::Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC::Conectar**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




