---
title: Función AllocFixupInfo (NapUtil.h)
description: Asigna memoria para una estructura FixupInfo del tamaño especificado.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- Función NAP AllocFixupInfo
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95ce329a433439716700b6ffc990d446c5d22faab91fa256f6abc0c73734327d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803495"
---
# <a name="allocfixupinfo-function"></a>Función AllocFixupInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función AllocFixupInfo** asigna memoria para una [**estructura FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) del tamaño especificado.

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fixupInfo* \[ in, out\]
</dt> <dd>

Puntero a la dirección de una estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) recién asignada.

</dd> <dt>

*countResultCodes* \[ En\]
</dt> <dd>

Número de códigos de resultado que se asignarán *a fixupInfo.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                   | Descripción                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se ha completado correctamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se pasó un argumento no válido.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | El sistema está sin memoria virtual. Se ha dado error en esta operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Todas las interfaces COM compatibles con el sistema NAP usan reglas de administración de memoria COM estándar y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   **El** autor de la llamada asigna y libera los parámetros de .
-   **El** destinatario asigna los parámetros out y el autor de la llamada lo libera **mediante CoTaskMem**.
-   **El autor de** la llamada asigna los parámetros de entrada y salida, los libera y reasigna el destinatario y, en última instancia, los libera el autor de la llamada, mediante **CoTaskMem**.

Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 





