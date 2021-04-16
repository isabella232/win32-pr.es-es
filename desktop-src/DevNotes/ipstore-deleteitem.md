---
description: Elimina el elemento especificado del almacenamiento protegido.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: IPStore::D método eleteItem (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650020"
---
# <a name="ipstoredeleteitem-method"></a>IPStore::D método eleteItem

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Elimina el elemento especificado del almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ de de\]
</dt> <dd>

Área de almacenamiento del proveedor.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección usuario actual del registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección del equipo local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ de\]
</dt> <dd>

Un puntero a un **GUID** que identifica el tipo de datos del elemento que se va a eliminar.

</dd> <dt>

*pItemSubType* \[ de\]
</dt> <dd>

**GUID** que indica el subtipo de elemento que se va a eliminar.

</dd> <dt>

*szItemName* \[ de\]
</dt> <dd>

Cadena que contiene el nombre del elemento que se va a eliminar.

</dd> <dt>

*pPromptInfo* \[ de\]
</dt> <dd>

Puntero a una estructura [**\_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Especifica la interfaz de usuario y los comportamientos de seguridad para la operación de eliminación.



| Value                                                                                                                                                                                                                                             | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**Archivo pst \_ SIN \_ \_ migración de IU**</dt> <dt>0x00000010</dt> </dl> | No mostrar la interfaz de usuario a menos que se requiera una contraseña personalizada.<br/> |



 

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
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
