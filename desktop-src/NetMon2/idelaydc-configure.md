---
description: El método configure envía la información de configuración utilizada para una captura.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Método IDelaydCConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496990"
---
# <a name="idelaydcconfigure-method"></a>IDelaydC:: Configure (método)

El método **Configure** envía la información de configuración utilizada para una captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConfigurationBlob* \[ de\]
</dt> <dd>

Identificador del BLOB que contiene la información de configuración.

</dd> <dt>

*hErrorBlob* \[ enuncia\]
</dt> <dd>

Identificador de un BLOB de error que contiene información de error adicional. Para obtener información sobre el contenido de un BLOB de error, consulte la sección Comentarios de este tema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                      | Descripción                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_**</dt> </dl>                  | El NPP informa de que se ha iniciado la sesión de captura.<br/>                          |
| <dl> <dt>**\_disco NMERR \_ no \_ local \_ fijo**</dt> </dl>    |                                                                                           |
| <dl> <dt>**NMERR \_ \_ no pudo \_ crear la \_ memoria**</dt> </dl> |                                                                                           |
| <dl> <dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt> </dl>            | No había memoria disponible. Cierre Windows para liberar recursos.<br/>               |
| <dl> <dt>**NMERR \_ parámetro no válido \_**</dt> </dl>         | El BLOB de configuración especificado por el parámetro hConfiguration no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido, pero no está desconectado.

El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de configuración especificado en *hConfigurationBlob*. El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.

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

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




