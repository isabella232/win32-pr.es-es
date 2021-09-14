---
description: Comprueba y descarga un objeto ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: IeAxiService::Initialize (Método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073694"
---
# <a name="ieaxiserviceinitialize-method"></a>IeAxiService::Initialize (Método)

El **método Initialize** comprueba y descarga un ActiveX objeto . Si el objeto cumple los requisitos de directiva, este método inicializa un objeto del sistema que instala el objeto ActiveX.

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

*hwndParent* \[ En\]
</dt> <dd>

Identificador de la ventana primaria de la ventana que está intentando instalar el control ActiveX.

</dd> <dt>

*dwClientPID* \[ En\]
</dt> <dd>

Identificador de proceso del proceso que realiza la llamada.

</dd> <dt>

*bstrDesktop* \[ En\]
</dt> <dd>

El escritorio para el objeto .

</dd> <dt>

*bstrClsID* \[ En\]
</dt> <dd>

Identificador de clase del objeto ActiveX que se debe instalar.

</dd> <dt>

*bstrURL* \[ En\]
</dt> <dd>

Dirección URL del objeto ActiveX que se instalará.

</dd> <dt>

*pbstrNonce* \[ out\]
</dt> <dd>

Contexto que se puede usar para compartir información de estado en llamadas a otros métodos usados para comprobar y descargar el ActiveX objeto.

</dd> <dt>

*ppISyncBrokerInterface* \[ out\]
</dt> <dd>

Puntero a la instancia de la [**interfaz IeAxiSystemInstaller**](ieaxisysteminstaller.md) que instala ActiveX control .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Código o valor devuelto                                                                                                                                                              | Descripción                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**TRUST \_ E \_ ASUNTO NO DE \_ \_ CONFIANZA**</dt> <dt>0x800B0004</dt> </dl> | El ActiveX no debe instalarse.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




