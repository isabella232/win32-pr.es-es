---
description: Abre un elemento para varios accesos.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'IPStore:: OpenItem (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670357"
---
# <a name="ipstoreopenitem-method"></a>IPStore:: OpenItem (método)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Abre un elemento para varios accesos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
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

Un puntero a un GUID que identifica el tipo de datos del elemento que se va a abrir.

</dd> <dt>

*pItemSubtype* \[ de\]
</dt> <dd>

Un puntero a un GUID que indica el subtipo de elemento que se va a abrir.

</dd> <dt>

*szItemName* \[ de\]
</dt> <dd>

Cadena que contiene el nombre del elemento que se va a abrir.

</dd> <dt>

*ModeFlags* \[ de\]
</dt> <dd>

Describe los modos de acceso a los que pertenece un conjunto especificado de cláusulas de acceso. Para obtener más información, vea [**PStore Types**](pstore-types.md).



| Value                                                                                                                                                                                                         | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**Archivo pst \_ LEER**</dt> <dt>0x0001</dt> </dl>    | Modo de acceso de lectura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**Archivo pst \_ ESCRIBIR**</dt> <dt>0x0002</dt> </dl> | Modo de acceso de escritura.<br/> |



 

</dd> <dt>

*pProomptInfo* \[ de\]
</dt> <dd>

Puntero a una estructura [**\_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Reserved: debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un valor **HRESULT** . Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.

## <a name="remarks"></a>Observaciones

El uso de **OpenItem** para abrir un elemento en la base de datos de almacenamiento protegido requiere que finalmente se cierre mediante [**IPStore:: CloseItem**](ipstore-closeitem.md) para evitar una pérdida de memoria.

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

 

 
