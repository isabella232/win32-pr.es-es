---
description: Cierra un elemento de datos especificado del almacenamiento protegido.
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: Método IPStore::CloseItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CloseItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 54ebcc20686a09344990af5dc742d018f4e2a19d9ca8669b6a90bd4563014173
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001635"
---
# <a name="ipstorecloseitem-method"></a>Método IPStore::CloseItem

\[La Storage protegida (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Cierra un elemento de datos especificado del almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloseItem(
  [in]       PST_KEY Key,
  [in] const PSGUID  *pItemType,
  [in] const GUID    *pItemSubtype,
  [in]       LPCWSTR *szItemName,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Especifica si el tipo es local en el equipo o solo está asociado al usuario que lo crea.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Clave \_ actual \_ del usuario**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección de usuario actual del Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Clave \_ de \_ máquina local**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección del equipo local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ En\]
</dt> <dd>

Puntero a un **GUID que** identifica el tipo de datos del elemento que se cerrará.

</dd> <dt>

*pItemSubtype* \[ En\]
</dt> <dd>

Puntero a un **GUID que** indica el subtipo de elemento que se cerrará.

</dd> <dt>

*szItemName* \[ En\]
</dt> <dd>

Cadena que contiene el nombre del elemento que se cerrará.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado: debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un valor HRESULT.** Un valor de **PST \_ E OK \_ indica** que la función se ha realizado correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
