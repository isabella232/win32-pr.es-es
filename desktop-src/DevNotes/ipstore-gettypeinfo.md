---
description: Recupera información asociada a un tipo.
ms.assetid: 27a283a5-8924-4a2f-8f58-e673a424e28a
title: Método IPStore::GetTypeInfo (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetTypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 67098a4f40fcfcc2ef0fedfcfd8d2ee48139e9c9687e53dd9ba0afb89fd1b983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079825"
---
# <a name="ipstoregettypeinfo-method"></a>Método IPStore::GetTypeInfo

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Recupera información asociada a un tipo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Especifica si el tipo es local para el equipo o solo está asociado al usuario que crea.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Clave \_ de \_ usuario actual**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección de usuario actual del Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CLAVE \_ LOCAL \_ MACHINE**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección máquina local del registro.<br/> |



 

</dd> <dt>

*pType* \[ En\]
</dt> <dd>

Puntero a un **GUID** que identifica el tipo de datos del almacenamiento.

</dd> <dt>

*ppInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ TYPEINFO de PST**](pst-typeinfo.md) que contiene el nombre del tipo de datos.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado: debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un **valor HRESULT.** Un valor de **PST \_ E OK \_ indica** que la función se ha realizado correctamente.

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

 

 
