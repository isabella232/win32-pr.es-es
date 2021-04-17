---
description: Cierra un elemento de datos especificado de un almacenamiento protegido.
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: 'IPStore:: CloseItem (método) (pstore. h)'
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
ms.openlocfilehash: e5f550df0ffa4dd2f35a91e768d70bb0359b9a4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670813"
---
# <a name="ipstorecloseitem-method"></a>IPStore:: CloseItem (método)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Cierra un elemento de datos especificado de un almacenamiento protegido.

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

*Clave* \[ de de\]
</dt> <dd>

Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección usuario actual del registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección del equipo local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ de\]
</dt> <dd>

Un puntero a un **GUID** que identifica el tipo de datos del elemento que se va a cerrar.

</dd> <dt>

*pItemSubtype* \[ de\]
</dt> <dd>

Un puntero a un **GUID** que indica el subtipo de elemento que se va a cerrar.

</dd> <dt>

*szItemName* \[ de\]
</dt> <dd>

Cadena que contiene el nombre del elemento que se va a cerrar.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Reserved: debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un valor **HRESULT** . Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
