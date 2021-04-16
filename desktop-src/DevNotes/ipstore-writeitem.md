---
description: Escribe un elemento de datos en el almacenamiento protegido.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'IPStore:: WriteItem (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650038"
---
# <a name="ipstorewriteitem-method"></a>IPStore:: WriteItem (método)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Escribe un elemento de datos en el almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
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

Un puntero a un **GUID** que identifica el tipo de datos del elemento de datos que se va a escribir.

</dd> <dt>

*pItemSubtype* \[ de\]
</dt> <dd>

Un puntero a un **GUID** que identifica el subtipo de datos del elemento de datos que se está escribiendo.

</dd> <dt>

*szItemName* \[ de\]
</dt> <dd>

Puntero a una cadena que contiene el nombre asignado al elemento de datos almacenado.

</dd> <dt>

*cbData* \[ enuncia\]
</dt> <dd>

Un puntero a un **valor DWORD** que indica el tamaño del búfer que contiene el elemento de datos almacenado.

</dd> <dt>

*ppbData* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que contiene el elemento de datos que se va a escribir.

</dd> <dt>

*pProomptInfo* \[ de\]
</dt> <dd>

Puntero a una [**estructura \_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwDefaultConfirmationStyle* \[ de\]
</dt> <dd>

El estilo de confirmación predeterminado.



| Value                                                                                                                                                                                                                             | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**Archivo pst \_ CF \_ default**</dt> <dt>0x00000000</dt> </dl> | Permite al usuario elegir el estilo de confirmación. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**Archivo pst \_ CF \_ ninguno**</dt> <dt>0x00000001</dt> </dl>          | Fuerza la creación del elemento silencioso. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

La interfaz de usuario y los comportamientos de seguridad para la operación de escritura.



| Value                                                                                                                                                                                                                                                              | Significado                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**Archivo pst \_ NO \_ sobrescribir**</dt> <dt>0x00000002</dt> </dl>                            | Especifica que el elemento se creará en el almacenamiento protegido. No se permite la sobrescritura de un elemento existente.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**Archivo pst \_ No RESTRINGIdo de \_ ITEMDATA**</dt> <dt>0x00000004</dt> </dl> | Especifica que el flujo de datos no es seguro. De forma predeterminada, las llamadas a elementos son seguras.<br/>                         |



 

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

 

 
