---
description: Comprueba y descarga un ActiveX objeto .
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
ms.openlocfilehash: 911d955f84d81b225a1b4062e47b2b9b6ab6d058aa6df2e6a72a8d40242345a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414895"
---
# <a name="ieaxiserviceinitialize-method"></a>IeAxiService::Initialize (Método)

El **método Initialize** comprueba y descarga un ActiveX objeto . Si el objeto cumple los requisitos de directiva, este método inicializa un objeto del sistema que instala ActiveX objeto.

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

El escritorio del objeto.

</dd> <dt>

*bstrClsID* \[ En\]
</dt> <dd>

Identificador de clase del objeto ActiveX instalar.

</dd> <dt>

*bstrURL* \[ En\]
</dt> <dd>

Dirección URL del objeto ActiveX instalar.

</dd> <dt>

*pbstrNonce* \[ out\]
</dt> <dd>

Contexto que se puede usar para compartir información de estado en llamadas a otros métodos usados para comprobar y descargar el ActiveX objeto.

</dd> <dt>

*ppISyncBrokerInterface* \[ out\]
</dt> <dd>

Puntero a la instancia de la [**interfaz IeAxiSystemInstaller**](ieaxisysteminstaller.md) que instala el control ActiveX control .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Código o valor devuelto                                                                                                                                                              | Descripción                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**TRUST \_ E \_ ASUNTO \_ NO \_ DE**</dt> <dt>CONFIANZA 0x800B0004</dt> </dl> | El ActiveX no debe instalarse.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




