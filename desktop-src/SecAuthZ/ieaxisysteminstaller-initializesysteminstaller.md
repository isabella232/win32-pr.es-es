---
description: Instala el objeto ActiveX especificado.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'IeAxiSystemInstaller:: InitializeSystemInstaller (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912430"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>IeAxiSystemInstaller:: InitializeSystemInstaller (método)

El método **InitializeSystemInstaller** instala el objeto ActiveX especificado.

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

*bstrUrl* \[ de\]
</dt> <dd>

Dirección URL del objeto ActiveX que se va a instalar.

</dd> <dt>

*dwClientPID* \[ de\]
</dt> <dd>

IDENTIFICADOR de proceso del proceso que realiza la llamada.

</dd> <dt>

*pCallback* \[ de\]
</dt> <dd>

Puntero a una instancia de la interfaz [**IeAxiServiceCallback**](ieaxiservicecallback.md) que comprueba si se permite instalar el objeto ActiveX.

</dd> <dt>

*pbstrNonce* \[ enuncia\]
</dt> <dd>

Contexto que se puede utilizar para compartir información de estado en llamadas a otros métodos utilizados para comprobar y descargar el objeto ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller se define como a50ea6f8-4764-4299-B309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

