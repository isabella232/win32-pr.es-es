---
title: Método INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent.h)
description: NapAgent llama a para consultar la solicitud soH del agente de mantenimiento del sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Método NAP de GetSoHRequest
- Método NAP de GetSoHRequest, interfaz INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP , GetSoHRequest method
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
ms.openlocfilehash: 96b9770607685dbd69e115f4f18d646b6d552fae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071642"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>Método INapSystemHealthAgentCallback::GetSoHRequest

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent llama al método **INapSystemHealthAgentCallback::GetSoHRequest** para consultar la solicitud soH del agente de mantenimiento del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*solicitud* \[ En\]
</dt> <dd>

Puntero COM a un [**objeto INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica el objeto de solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                                                      | Descripción                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                             | Indica que se completó correctamente.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ DE \_ WIN32 (EL SERVIDOR RPC \_ S NO ESTÁ \_ \_ DISPONIBLE)**</dt> </dl> | Si la implementación devuelve este código, NapAgent quita sha de la lista de SHA enlazado y vacía su entrada de caché.<br/> |



 

Cuando la implementación devuelve cualquier valor devuelto (excepto **HRESULT \_ FROM \_ WIN32(RPC \_ S SERVER \_ \_ UNAVAILABLE)**) , el sistema NAP crea y devuelve un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) al SHV correspondiente con los siguientes tipos y valores de atributo:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) =  &lt; Id&gt;
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  &lt; código de error&gt;

## <a name="remarks"></a>Observaciones

El sistema NAP declara este método de devolución de llamada y lo va a implementar el escritor SHA.

Este método debe procesar la solicitud y devolver inmediatamente. Retrasar la devolución de este método afecta negativamente al rendimiento y la capacidad de respuesta del sistema, y puede hacer que otras partes del sistema operativo se quejen del tiempo de espera.

La supervisión del estado de mantenimiento no debe realizarse como parte de esta llamada, especialmente si el cálculo es intensivo y tarda mucho tiempo. La supervisión del estado de mantenimiento y el cálculo de SoH deben realizarse en un subproceso o servicio independiente. La única función de este método debe ser establecer el SoH y la devolución de SHA.

Si el SHA va a tardar mucho tiempo en generar un SoH, el SoH almacenado en caché debe devolverse a NapAgent. Si no hay ningún SoH almacenado en caché para devolver, sha debe devolver inmediatamente un SoH con los siguientes tipos y valores de atributo:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) =  &lt; Id&gt;
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E NO CACHED \_ \_ \_ SOH**](nap-error-constants.md)

Cuando se ha generado el SoH, sha debe llamar a [**INapSystemHealthAgentBinding::NotifySoHChange para**](inapsystemhealthagentbinding-notifysohchange-method.md) notificar al NapAgent el cambio de estado del sistema.

NapAgent llama a este método para consultar el SoHRequest del agente de mantenimiento del sistema. Sha puede consultar el objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) pasado para ver los parámetros que necesita para calcular soHRequest. Sha debe establecer el SoHRequest calculado en el objeto de solicitud. Sha no debe contener referencias al objeto de solicitud una vez completada esta llamada.

Cuando se llama a este método, si hay un SoH en la caché de NapAgent, se establece en el objeto de solicitud. Sha puede consultarlo mediante **GetSoHRequest.** Si sha no establece un soH nuevo, se usa el almacenado en caché.

En el caso de las SHA sin enlazar registradas con el sistema, el sistema NAP crea y envía un SoHRequest a la SHV correspondiente con los siguientes tipos y valores de atributo:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) =  &lt; Id&gt;
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E NO \_ \_ INICIALIZADO**](nap-error-constants.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





