---
title: Método IEnumProgressItems RemoteNext
description: Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración. | Método IEnumProgressItems RemoteNext
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Método IMAPI de RemoteNext
- Método IMAPI de RemoteNext, interfaz IEnumProgressItems
- Interfaz IEnumProgressItems IMAPI, método RemoteNext
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daa2b33fdc356782837aadfe37186bc4cc2b493208fdc78ba645ada9e746582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884855"
---
# <a name="ienumprogressitemsremotenext-method"></a>IEnumProgressItems::RemoteNext (método)

Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
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

Matriz [**de interfaces IProgressItem.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) Debe liberar cada interfaz en rgelt cuando haya terminado.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Número de elementos devueltos en rgelt. Puede establecer *pceltFetched en* **NULL** si *celt* es uno. De lo contrario, inicialice el *valor de pceltFetched* en 0 antes de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

S OK se devuelve cuando el número de elementos solicitados (celt ) se devuelve correctamente o el número de elementos devueltos \_ *(pceltFetched)* es menor que el número de elementos solicitados.

Se pueden devolver otros códigos de éxito como resultado de la implementación. Los siguientes códigos de error se devuelven normalmente cuando se produce un error en la operación, pero no representan los únicos valores de error posibles:



| Código devuelto                                                                                   | Descripción                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El puntero no es válido.<br/> Valor: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No se pudo asignar la memoria necesaria.<br/> Valor: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o varios argumentos no son válidos.<br/> Valor: 0x80070057<br/>    |
| <dl> <dt>**E \_ INESPERADO**</dt> </dl> | Error inesperado.<br/> Valor: 0x8000FFFF<br/>         |



 

## <a name="remarks"></a>Comentarios

Si quedan menos elementos que el número solicitado de elementos en la secuencia, recupera los elementos restantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Idl<br/>                      | <dl> <dt>Imapi2fs.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumProgressItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[IEnumProgressItems::Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





