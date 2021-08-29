---
title: Método IEnumFsiItems RemoteNext
description: Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración. | Método IEnumFsiItems RemoteNext
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Método IMAPI de RemoteNext
- Método IMAPI de RemoteNext, interfaz IEnumFsiItems
- Interfaz IEnumFsiItems IMAPI, método RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b63c2d0a5223dd2ae282804b2a6dc5e2872a5c108ed885bdca5a0db862a4b75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062548"
---
# <a name="ienumfsiitemsremotenext-method"></a>IEnumFsiItems::RemoteNext (Método)

Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de elementos que se recuperarán.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Matriz [**de interfaces IFsiItem.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) Debe liberar cada interfaz en rgelt cuando haya terminado.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Número de elementos devueltos en rgelt. Puede establecer *pceltFetched en* **NULL si** *celt* es uno. De lo contrario, inicialice el *valor de pceltFetched* en 0 antes de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

S OK se devuelve cuando el número de elementos solicitados (celt ) se devuelve correctamente o el número de elementos devueltos \_ *(pceltFetched)* es menor que el número de elementos solicitados.

Se pueden devolver otros códigos de éxito como resultado de la implementación. Los siguientes códigos de error se devuelven normalmente cuando se produce un error en la operación, pero no representan los únicos valores de error posibles:



| Código devuelto                                                                                   | Descripción                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El puntero no es válido.<br/> Valor: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No se pudo asignar la memoria necesaria.<br/> Valor: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o varios argumentos no son válidos.<br/> Valor: 0x80070057<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Idl<br/>                      | <dl> <dt>Imapi2fs.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumFsiItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[IEnumFsiItems::Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





