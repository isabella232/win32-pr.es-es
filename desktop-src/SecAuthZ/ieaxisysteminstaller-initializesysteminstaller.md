---
description: Instala el objeto ActiveX especificado.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: IeAxiSystemInstaller::InitializeSystemInstaller (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160822"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>IeAxiSystemInstaller::InitializeSystemInstaller (método)

El **método InitializeSystemInstaller** instala el objeto ActiveX especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrUrl* \[ En\]
</dt> <dd>

Dirección URL del objeto ActiveX que se instalará.

</dd> <dt>

*dwClientPID* \[ En\]
</dt> <dd>

Identificador de proceso del proceso que realiza la llamada.

</dd> <dt>

*pCallback* \[ En\]
</dt> <dd>

Puntero a una instancia de la [**interfaz IeAxiServiceCallback**](ieaxiservicecallback.md) que comprueba si el objeto ActiveX se puede instalar.

</dd> <dt>

*pbstrNonce* \[ out\]
</dt> <dd>

Contexto que se puede usar para compartir información de estado en llamadas a otros métodos usados para comprobar y descargar el ActiveX objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller se define como a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

