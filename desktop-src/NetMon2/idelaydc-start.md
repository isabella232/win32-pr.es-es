---
description: El método start inicia una captura.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'IDelaydC:: Start (método) (Netmon. h)'
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
ms.openlocfilehash: a912af44dddb8a25d3279a5cdd7f021646c26e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686563"
---
# <a name="idelaydcstart-method"></a>IDelaydC:: Start (método)

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



| Código devuelto                                                                                           | Descripción                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl> | La captura está en un estado de pausa y debe detenerse antes de que se pueda reiniciar. Llame a [**IDelaydC:: Stop**](idelaydc-stop.md) para detener la captura. Para obtener más información, consulte la sección Comentarios de este tema.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>       | La captura ya se ha iniciado.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>  | NPP no está conectado a la red. Llame a [**IDelaydC:: Connect**](idelaydc-connect.md) para conectarse a la red.<br/>                                                                                          |
| <dl> <dt>**NMERR \_ no \_ retrasado**</dt> </dl>    | NPP está conectado a la red, pero no con el método [**IDelaydC:: Connect**](idelaydc-connect.md) .<br/>                                                                                                      |



 

## <a name="remarks"></a>Observaciones

La ubicación del [*archivo de captura*](c.md) se especifica en el registro de Windows, pero puede usar Monitor de red para cambiar la ubicación del archivo.

Para reiniciar la captura mediante **IDelaydC:: Start** y [**IDelaydC:: Stop**](idelaydc-stop.md), debe llamar al método [**IDelaydC:: configure**](idelaydc-configure.md) para volver a configurar la conexión cada vez que llame al método **IDelaydC:: Start** para reiniciar la captura de datos. Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.

> [!Note]  
> También puede iniciar y detener la captura mediante los métodos [**IDelaydC::P ause**](idelaydc-pause.md) y [**IDelaydC:: resume**](idelaydc-resume.md) . Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.

 

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

[**IDelaydC:: configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




