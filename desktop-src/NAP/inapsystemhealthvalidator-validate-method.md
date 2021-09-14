---
title: Método INapSystemHealthValidator Validate (NapSystemHealthValidator.h)
description: El sistema NAP para validar el SoHRequest recibido de un cliente.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validación del método NAP
- Validación del método NAP, interfaz INapSystemHealthValidator
- Nap de interfaz INapSystemHealthValidator , método Validate
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161273"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>INapSystemHealthValidator::Validate (Método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El desarrollador de SHV define el método **INapSystemHealthValidator::Validate** y lo llama el sistema NAP para validar el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recibido de un cliente.

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

*solicitud* \[ En\]
</dt> <dd>

Puntero COM a un [**objeto INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que identifica el objeto de solicitud de validación.

</dd> <dt>

*hintTimeOutInMsec* \[ En\]
</dt> <dd>

Duración, en milisegundos, del período de tiempo de espera de comunicación. El validador de estado del sistema (SHV) debe responder dentro de esta cantidad de tiempo; De lo contrario, se descarta la respuesta.

> [!Note]  
> El tiempo de espera predeterminado para todas las SHV es de 2000 milisegundos. El uso de un valor distinto del predeterminado cambiará el tiempo de espera de todos los SHV registrados.

 

</dd> <dt>

*Devolución de llamada* \[ En\]
</dt> <dd>

Puntero al objeto de devolución de llamada [**INapServerCallback**](inapservercallback.md). Los SHV usan este puntero de devolución de llamada cuando **devuelven E \_ PENDING** desde la llamada a **INapSystemHealthValidator::Validate**. Se usa para la validación asincrónica. Se espera que los SHV respondan dentro de la *hora hintTimeOutInMsec* o, de lo contrario, se descartará la respuesta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se devuelve cualquier otro código de error, el sistema asume que se ha producido un error serverComponent y que se realiza la asignación adecuada para pasar o producir un error.



| Código devuelto                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Indica que el validador ha establecido un SoHResponse en el objeto "request".<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ PENDIENTE**</dt> </dl>                  | Indica que se llamará a OnComplete() en un subproceso independiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**SERVIDOR \_ RPC S NO \_ \_ DISPONIBLE**</dt> </dl> | Indica que el proceso de validador de estado del sistema (SHV) finalizó sin que NapServer liberara realmente una referencia a él. NapServer intentará volver a crear una nueva referencia a la SHV y volverá a ejecutar la llamada Validate una vez. Si se produce un error en la creación del objeto o la validación que se vuelve a ejecutar, el SHV se quita de la lista de SHV cargados. La única manera de volver a cargar este SHV es anular el registro y volver a registrar la SHV, o cuando se reinicie NapServer.<br/> |



 

## <a name="remarks"></a>Observaciones

Para admitir la detección de intrusiones, se pedirá a los SHV que validen la máquina cliente independientemente de si el cliente envió un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a la SHV.

La SHV debe hacer lo siguiente:

-   Recupere [**soHRequest de**](/windows/win32/api/naptypes/ns-naptypes-soh) la *solicitud mediante* una llamada a [**request. GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Si el [**paquete SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) es NULL:
    -   Si el SHV es un sistema de detección de intrusiones, rellene un paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con el código de [**error nap**](nap-error-constants.md) adecuado para saber por qué la máquina cliente es malintencionada.
    -   Todas las demás SHV deben rellenar un [**paquete SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con un código de error [**de NAP E MISSING \_ \_ \_ SOH**](nap-error-constants.md).
-   Si *napSystemGenerated es* **TRUE** desde la llamada a [**la solicitud. GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), la SHV debe esperar un paquete [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) con los tres TLV siguientes: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. NapAgent genera este **SoHRequest** en nombre del Agente de mantenimiento del sistema (SHA), ya que se produjo un error al recuperar un paquete de solicitud de SHA.
-   Valide [**el paquete SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)
    -   Si [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) tiene un formato correcto, cree un paquete **SoHResponse** con el código de error [**NAP E INVALID \_ \_ \_ PACKET**](nap-error-constants.md).
    -   Si la SHV solo usa información almacenada en caché para validar el paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (es decir, no se realiza  ninguna E/S), puede construir **soHResponse**, establecerlo en el objeto en la solicitud y devolver **S \_ OK**.
    -   Si la SHV está realizando E/S con el fin de hablar con sus servidores back-end para validar el estado del cliente, debe poner en cola la E/O y devolver esta función con **E \_ PENDING**. En este caso, la SHV debe llamar a la [**devolución de llamada. OnComplete() en**](inapservercallback-oncomplete-method.md) un subproceso independiente dentro del período de tiempo de espera, *hintTimeOutInMsec*. De lo contrario, se descartará la respuesta del SHV.
-   No devuelva ningún otro error distinto de los enumerados anteriormente. Si la SHV devuelve cualquier otro código de error (por ejemplo, error del sistema), el paquete se descartará.

Una SHV debe devolver un TLV **sohAttributeTypeComplianceResultCodes** o **sohAttributeTypeFailureCategory** en [**su soHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

-   [**sohAttributeTypeComplianceResultCodes TLV:**](sohattributetype-enum.md)si la SHV puede validar el estado del cliente (es decir, correcto o incorrecto), se devuelve este TLV.
-   [**sohAttributeTypeFailureCategory TLV:**](sohattributetype-enum.md)si se ha producido algún error de componente o comunicación en el cliente o servidor, este TLV debe indicarlo. Este TLV se asignará aún más a correcto o incorrecto en función de la configuración del SHV. Para obtener más información, vea la [**interfaz INapServerManagement**](inapservermanagement.md) y la [**estructura FailureCategoryMapping.**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)

La SHV no debe contener referencias a la *solicitud o* *devolución de llamada* una vez completada la llamada asincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





