---
description: Devuelve el puntero de interfaz de un subtipo para enumerar elementos en la base de datos de almacenamiento protegida.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: Método IPStore::EnumItems (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0b0ea4976dcfdfe2a099362e9a937ac69144bd678965c6a308cb96fed2a3c88b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001515"
---
# <a name="ipstoreenumitems-method"></a>Método IPStore::EnumItems

\[La Storage protegida (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Devuelve el puntero de interfaz de un subtipo para enumerar elementos en la base de datos de almacenamiento protegida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
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
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Clave \_ de \_ máquina local**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección del equipo local del Registro.<br/> |



 

</dd> <dt>

*pItemType* \[ En\]
</dt> <dd>

Puntero a un **GUID que** identifica el tipo de datos del elemento que se enumerará.

</dd> <dt>

*pItemSubtype* \[ En\]
</dt> <dd>

Puntero a un **GUID que** identifica el subtipo de datos del elemento que se enumerará.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado: debe establecerse en cero.

</dd> <dt>

*losaum* \[ En\]
</dt> <dd>

Puntero a un puntero a una [**interfaz IEnumPStoreItems.**](ienumpstoreitems.md)

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

 

 
