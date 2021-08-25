---
title: Función AllocCountedString (NapUtil.h)
description: Asigna memoria para una cadena terminada en NULL y la devuelve en una estructura CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- Función AllocCountedString NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef205cf7211f25253a3e6ba0cb7cd84ac37dbdb49848b36e844595d632552331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891745"
---
# <a name="alloccountedstring-function"></a>Función AllocCountedString

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función AllocCountedString** asigna memoria para una cadena terminada en NULL y la devuelve en una [**estructura CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*countedString* \[ in, out\]
</dt> <dd>

Puntero a la dirección de una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) recién asignada.

</dd> <dt>

*string* \[ En\]
</dt> <dd>

Puntero a la cadena terminada en NULL que se va a devolver en *countedString.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                   | Descripción                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se ha completado correctamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se pasó un argumento no válido.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | El sistema está sin memoria virtual. Error en esta operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Todas las interfaces COM compatibles con el sistema NAP usan reglas de administración de memoria COM estándar y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   **En,** el autor de la llamada asigna y libera los parámetros.
-   **El** destinatario asigna los parámetros out y los libera el autor de la llamada mediante **CoTaskMem.**
-   **El autor de** la llamada asigna los parámetros de entrada y salida, los libera y reasigna el destinatario y, en última instancia, los libera el autor de la llamada, mediante **CoTaskMem**.

Todas las funciones nap para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FreeCountedString**](freecountedstring-func.md)
</dt> </dl>

 

 





