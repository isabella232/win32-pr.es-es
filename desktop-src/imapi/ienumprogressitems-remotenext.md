---
title: IEnumProgressItems RemoteNext, método
description: Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración. | IEnumProgressItems RemoteNext, método
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Método RemoteNext IMAPi
- Método RemoteNext IMAPi, interfaz IEnumProgressItems
- Interfaz IEnumProgressItems IMAPi, método RemoteNext
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
ms.openlocfilehash: a088a1be640c6653a8a8ccd8b00cf21bd027ecd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105707685"
---
# <a name="ienumprogressitemsremotenext-method"></a>IEnumProgressItems:: RemoteNext (método)

Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración.

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

*Celt* \[ de\]
</dt> <dd>

Número de elementos que se van a recuperar.

</dd> <dt>

*rgelt* \[ enuncia\]
</dt> <dd>

Matriz de interfaces [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) . Debe liberar cada interfaz en rgelt cuando haya terminado.

</dd> <dt>

*pceltFetched* \[ enuncia\]
</dt> <dd>

Número de elementos devueltos en rgelt. Puede establecer *pceltFetched* en **null** si *Celt* es uno. De lo contrario, inicialice el valor de *pceltFetched* en 0 antes de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

\_Se devuelve S OK cuando el número de elementos solicitados (*Celt*) se devuelve correctamente o el número de elementos devueltos (*pceltFetched*) es menor que el número de elementos solicitados.

Se pueden devolver otros códigos de éxito como resultado de la implementación de. Los códigos de error siguientes se suelen devolver en caso de error en la operación, pero no representan los únicos valores de error posibles:



| Código devuelto                                                                                   | Descripción                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_puntero E**</dt> </dl>     | El puntero no es válido.<br/> Valor: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No se pudo asignar la memoria necesaria.<br/> Valor: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o varios argumentos no son válidos.<br/> Valor: 0x80070057<br/>    |
| <dl> <dt>**E \_ Inesperado**</dt> </dl> | Error inesperado.<br/> Valor: 0x8000FFFF<br/>         |



 

## <a name="remarks"></a>Observaciones

Si hay menos del número solicitado de elementos que quedan en la secuencia, recupera los elementos restantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con \[ solo aplicaciones de escritorio de SP2\]<br/>                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| IDL<br/>                      | <dl> <dt>Imapi2fs. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumProgressItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[IEnumProgressItems:: Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





