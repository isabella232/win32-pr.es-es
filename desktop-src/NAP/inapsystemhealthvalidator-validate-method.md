---
title: Método Validate de INapSystemHealthValidator (NapSystemHealthValidator. h)
description: El sistema NAP para validar el SoHRequest recibido de un cliente.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validar el método NAP
- Método Validate NAP, interfaz INapSystemHealthValidator
- Interfaz INapSystemHealthValidator NAP, método Validate
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676696"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>INapSystemHealthValidator:: Validate (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapSystemHealthValidator:: Validate** lo define el desarrollador de SHV y el sistema NAP lo llama para validar el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recibido de un cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*solicitud* \[ de de\]
</dt> <dd>

Puntero COM a un objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que identifica el objeto de solicitud de validación.

</dd> <dt>

*hintTimeOutInMsec* \[ de\]
</dt> <dd>

La duración, en milisegundos, del período de tiempo de espera de la comunicación. El validador de mantenimiento del sistema (SHV) debe responder en este período de tiempo; de lo contrario, se quita la respuesta.

> [!Note]  
> El tiempo de espera predeterminado para todos los SHV es de 2000 milisegundos. Si usa un valor distinto del predeterminado, se cambiará el tiempo de espera de todos los SHV registrados.

 

</dd> <dt>

*devolución de llamada* \[ de\]
</dt> <dd>

Un puntero al objeto de devolución de llamada [**INapServerCallback**](inapservercallback.md). Los SHV usan este puntero de devolución de llamada cuando devuelven **E \_ pendientes** de la llamada a **INapSystemHealthValidator:: Validate**. Se utiliza para la validación asincrónica. Se espera que los SHV respondan dentro del tiempo de *hintTimeOutInMsec* o, de lo contrario, se quitará la respuesta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se devuelve cualquier otro código de error, el sistema asume que se ha producido un error de serverComponent y se ha realizado la asignación adecuada a Pass/Fail.



| Código devuelto                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Indica que el validador ha establecido SoHResponse en el objeto ' request '.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ pendientes**</dt> </dl>                  | Indica que se llamará a alcomplete () en un subproceso independiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**el \_ servidor RPC S \_ \_ no está disponible**</dt> </dl> | Indica que el proceso de validador de mantenimiento del sistema (SHV) terminó sin que el NapServer realmente haya liberado una referencia a él. NapServer intentará volver a crear una nueva referencia al SHV y volverá a ejecutar la llamada de validación una vez. Si se produce un error en la creación del objeto o la validación que se ha vuelto a ejecutar, el SHV se quita de la lista de SHV cargados. La única forma en que se puede recargar ahora este SHV es anular el registro y volver a registrar el SHV, o bien cuando se reinicie NapServer<br/> |



 

## <a name="remarks"></a>Observaciones

Con el fin de admitir la detección de intrusiones, se pedirá a los SHV que validen el equipo cliente, independientemente de si el cliente envió un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado al SHV.

El SHV debe hacer lo siguiente:

-   Recupere el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) de la *solicitud* mediante una llamada a la [**solicitud. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Si el paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) es NULL:
    -   Si el SHV es un sistema de detección de intrusiones, rellene un paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con el [**código de error NAP**](nap-error-constants.md) adecuado en cuanto a la razón por la que el equipo cliente es malintencionado.
    -   Todos los demás SHV deben rellenar un paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con un código de error [**NAP \_ E \_ Missing \_ SOH**](nap-error-constants.md).
-   Si *napSystemGenerated* es **true** desde la llamada a la [**solicitud. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), el SHV debería esperar un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) con los 3 TLVs siguientes: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. Este **SoHRequest** lo genera NapAgent en nombre del agente de mantenimiento del sistema (SHA), ya que se produjo un error al recuperar un paquete de solicitud del Sha.
-   Valide el paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .
    -   Si el formato de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) es incorrecto, construya un paquete **SoHResponse** con código de error [**NAP \_ E \_ \_ paquete no válido**](nap-error-constants.md).
    -   Si el SHV solo usa información almacenada en caché para validar el paquete de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (es decir, no se realiza ninguna e/s), puede construir el **SoHResponse**, establecerlo en el objeto en la *solicitud* y devolver **S \_ correcto**.
    -   Si el SHV está realizando e/s para comunicarse con los servidores back-end para validar el estado del cliente, debe poner en cola la e/s y devolver esta función con **E \_ pendiente**. En este caso, el SHV debe llamar a [**callback. Alcompletar ()**](inapservercallback-oncomplete-method.md) en un subproceso independiente dentro del período de tiempo de espera, *hintTimeOutInMsec*. De lo contrario, se quitará la respuesta de SHV.
-   No devuelva ningún otro error distinto de los enumerados anteriormente. Si el SHV devuelve cualquier otro código de error (por ejemplo, error del sistema), se descartará el paquete.

Un SHV debe devolver un TLV de **sohAttributeTypeComplianceResultCodes** o **SohAttributeTypeFailureCategory** en su [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

-   [**TLV de sohAttributeTypeComplianceResultCodes**](sohattributetype-enum.md): Si el SHV podría validar el estado del cliente (es decir, correcto o incorrecto), se devuelve este TLV.
-   [**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md): si se produjo algún error de componente o de comunicación en el cliente o servidor, debe indicarse mediante este TLV. Este TLV se asignará a un estado correcto o incorrecto en función de la configuración de SHV. Para obtener más información, vea la interfaz [**INapServerManagement**](inapservermanagement.md) y la estructura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .

El SHV no debe contener referencias a *request* o *callback* una vez que se complete la llamada asyncronous.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





