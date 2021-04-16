---
title: Función AllocCountedString (NapUtil. h)
description: Asigna memoria para una cadena terminada en NULL y la devuelve en una estructura CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- AllocCountedString función NAP
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
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676585"
---
# <a name="alloccountedstring-function"></a>AllocCountedString función)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La función **AllocCountedString** asigna memoria para una cadena terminada en NULL y la devuelve en una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .

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

*cadena* \[ de\]
</dt> <dd>

Un puntero a la cadena terminada en null que se va a devolver en *countedString*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                   | Descripción                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | La operación se ha completado correctamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se pasó un argumento no válido.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | El sistema no tiene memoria virtual. No se pudo realizar esta operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   El autor de la llamada asigna y libera los parámetros **in** .
-   El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.
-   Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.

Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FreeCountedString**](freecountedstring-func.md)
</dt> </dl>

 

 





