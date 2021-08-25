---
description: Configura la preferencia de las funcionalidades predeterminadas.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: Método IH323LineEx::SetDefaultCapabilityPreferrence (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64eb3385edb758529f27f9fb90eb0cce998eca60f202c72a28ba48a5318c6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992085"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>Método IH323LineEx::SetDefaultCapabilityPreferrence

\[**SetDefaultCapabilityPreferrence** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método SetDefaultCapabilityPreferrence** configura la preferencia de las funcionalidades predeterminadas. Las funcionalidades tienen un peso predeterminado de 100. Si la aplicación especifica un peso mayor para una funcionalidad, tendrá una prioridad más alta durante la negociación de H.245. Si la aplicación establece el peso de una funcionalidad en 0, no se usará en la negociación H.245.

Este método es acumulativo. Por ejemplo, si se llama primero a este método para deshabilitar una funcionalidad y se llama de nuevo para deshabilitar otra, ambas funcionalidades se deshabilitarán como resultado de estas dos llamadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwNumCaps* \[ En\]
</dt> <dd>

Valor **DWORD** que contiene el número de funcionalidades establecidas con este método.

</dd> <dt>

*pCapabilities* \[ En\]
</dt> <dd>

Matriz de funcionalidades. Cada elemento de la matriz es un [**valor H245 \_ CAPABILITY.**](h245-capability.md)

</dd> <dt>

*pWeights* \[ En\]
</dt> <dd>

Matriz de pesos asociada a las funcionalidades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pCapabilities* es **NULL** o el parámetro *pWeights* es **NULL,** o tanto *pCapabilities* como *pWeights* son **NULL,** o la matriz pCapabilities contiene un objeto de funcionalidad H.245 no válido.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | No se puede leer un elemento de la *matriz pWeights* o un elemento de la *matriz pCapabilities.*<br/>                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




