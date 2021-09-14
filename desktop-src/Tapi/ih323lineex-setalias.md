---
description: El método SetAlias configura un alias H.323 predeterminado para la dirección. Este alias se usará en el intercambio de configuración de llamadas H.323 para que la otra parte conozca el nombre de esta entidad.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: Método IH323LineEx::SetAlias (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068753"
---
# <a name="ih323lineexsetalias-method"></a>IH323LineEx::SetAlias (método)

\[**SetAlias** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método SetAlias** configura un alias H.323 predeterminado para la dirección. Este alias se usará en el intercambio de configuración de llamadas H.323 para que la otra parte conozca el nombre de esta entidad.

Al llamar a este método una segunda vez, se sobrescribirá el alias anterior.

El alias establecido en esta interfaz solo se usará cuando no haya otra manera de que el TSP encuentre un alias adecuado. En el futuro, cuando se agrega compatibilidad con gatekeeper al TSP, el alias registrado en el equipo selector o asignado por el selector invalidará lo que se establezca a través de este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strAlias* \[ En\]
</dt> <dd>

Alias que se va a usar en Unicode. **No se** requiere la terminación NULL.

</dd> <dt>

*dwLength* \[ En\]
</dt> <dd>

Longitud del nombre de alias en número de caracteres, incluido el **terminador** nulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                               | Descripción                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método se realizó correctamente.<br/>                                                                                                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | El número de caracteres indicado en *dwLength* supera el número real de caracteres del *parámetro strAlias.*<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




