---
title: Método INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: El NapAgent llama a para consultar la solicitud de SoH del agente de mantenimiento del sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422402"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>INapSystemHealthAgentCallback:: GetSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El NapAgent llama al método **INapSystemHealthAgentCallback:: GetSoHRequest** para consultar la solicitud de SOH del agente de mantenimiento del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*solicitud* \[ de de\]
</dt> <dd>

Puntero COM a un objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica el objeto de solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                                                      | Descripción                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                             | Indica que se completó correctamente.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ de \_ Win32 ( \_ servidor RPC \_ \_ no disponible)**</dt> </dl> | Si la implementación devuelve este código, NapAgent quita el SHA de la lista Bound-SHA y vacía su entrada de caché.<br/> |



 

Cuando la implementación devuelve cualquier valor devuelto (excepto **HRESULT \_ de \_ Win32 ( \_ servidor RPC \_ \_ no disponible)**), el sistema NAP crea y devuelve un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) al SHV correspondiente con los siguientes valores y tipos de atributo:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <> código de error

## <a name="remarks"></a>Observaciones

Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.

Este método debe procesar la solicitud y volver inmediatamente. Retrasar la devolución de este método afecta negativamente al rendimiento y la capacidad de respuesta del sistema, y puede provocar que se agote el tiempo de espera de otras partes del sistema operativo.

La supervisión del estado de mantenimiento no debe realizarse como parte de esta llamada, especialmente si se trata de un proceso intensivo y tarda mucho tiempo. La supervisión del estado de mantenimiento y el cálculo de SoH deben realizarse en un subproceso o servicio independiente. La única función de este método debe ser establecer el SoH de SHA y devolver.

Si el SHA tarda mucho tiempo en generar un SoH, se debe devolver el SoH almacenado en caché a NapAgent. Si no hay ningún SoH almacenado en caché para devolver, el SHA debe devolver inmediatamente un SoH con los siguientes valores y tipos de atributo:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  NO se ha [ **\_ \_ \_ almacenado en caché el \_ SOH de NAP E**](nap-error-constants.md)

Cuando se ha generado el SoH, el SHA debe llamar a [**INapSystemHealthAgentBinding:: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para notificar al NapAgent el cambio de mantenimiento del sistema.

NapAgent llama a este método para consultar el SoHRequest del agente de mantenimiento del sistema. SHA puede consultar el objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) pasado en busca de los parámetros que necesita para calcular el SoHRequest. SHA debe establecer el SoHRequest calculado en el objeto de solicitud. SHA no debe contener referencias al objeto de solicitud una vez completada esta llamada.

Cuando se llama a este método, si hay un SoH en la memoria caché de NapAgent, se establece en el objeto de solicitud. SHA puede consultarlo mediante **GetSoHRequest**. Si el SHA no establece un nuevo SoH, se usa el almacenamiento en caché.

En el caso de los Sha sin enlazar que se registran con el sistema, el sistema NAP construye y envía un SoHRequest al SHV correspondiente con los siguientes valores y tipos de atributo:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ no \_ inicializado**](nap-error-constants.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





