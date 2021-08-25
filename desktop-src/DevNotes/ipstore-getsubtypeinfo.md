---
description: Recupera información asociada a un subtipo.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: Método IPStore::GetSubtypeInfo (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d97b1f710344acf2c635adb5109175d017fc568d87673f5565e1be5b22e06cf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749845"
---
# <a name="ipstoregetsubtypeinfo-method"></a>Método IPStore::GetSubtypeInfo

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Recupera información asociada a un subtipo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Área de almacenamiento del proveedor.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Clave \_ de \_ usuario actual**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección de usuario actual del Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CLAVE \_ LOCAL \_ MACHINE**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección máquina local del registro.<br/> |



 

</dd> <dt>

*pType* \[ En\]
</dt> <dd>

Puntero a un GUID que identifica el tipo de datos del almacenamiento.

</dd> <dt>

*pSubtype* \[ En\]
</dt> <dd>

Puntero a un GUID que identifica el subtipo de datos del almacenamiento.

</dd> <dt>

*ppInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ TYPEINFO de PST.**](pst-typeinfo.md)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado: debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un **valor HRESULT.** Un valor de PST \_ E OK indica que la función se ha realizado \_ correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PST \_ TYPEINFO**](pst-typeinfo.md)
</dt> </dl>

 

 
