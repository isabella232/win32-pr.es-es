---
description: Comprueba y descarga un objeto ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'IeAxiService:: Initialize (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278996"
---
# <a name="ieaxiserviceinitialize-method"></a>IeAxiService:: Initialize (método)

El método **Initialize** comprueba y descarga un objeto ActiveX. Si el objeto cumple los requisitos de la Directiva, este método inicializa un objeto del sistema que instala el objeto ActiveX.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Identificador de la ventana primaria de la ventana que está intentando instalar el control ActiveX.

</dd> <dt>

*dwClientPID* \[ de\]
</dt> <dd>

IDENTIFICADOR de proceso del proceso que realiza la llamada.

</dd> <dt>

*bstrDesktop* \[ de\]
</dt> <dd>

Escritorio del objeto.

</dd> <dt>

*bstrClsID* \[ de\]
</dt> <dd>

IDENTIFICADOR de clase del objeto ActiveX que se va a instalar.

</dd> <dt>

*bstrURL* \[ de\]
</dt> <dd>

Dirección URL del objeto ActiveX que se va a instalar.

</dd> <dt>

*pbstrNonce* \[ enuncia\]
</dt> <dd>

Contexto que se puede utilizar para compartir información de estado en llamadas a otros métodos utilizados para comprobar y descargar el objeto ActiveX.

</dd> <dt>

*ppISyncBrokerInterface* \[ enuncia\]
</dt> <dd>

Puntero a la instancia de la interfaz [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) que instala el control ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Código o valor devuelto                                                                                                                                                              | Descripción                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Confianza \_ de E \_ \_ no \_**</dt> es de confianza <dt>0x800B0004</dt> </dl> | El objeto ActiveX no debe estar instalado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




