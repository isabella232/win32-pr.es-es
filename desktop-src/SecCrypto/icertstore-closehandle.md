---
description: Cierra un identificador HCERTSTORE adquirido a través de la propiedad StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'ICertStore:: CloseHandle (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671849"
---
# <a name="icertstoreclosehandle-method"></a>ICertStore:: CloseHandle (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

El método **CloseHandle** cierra un identificador HCERTSTORE adquirido a través de la propiedad [**StoreHandle**](icertstore-storehandle.md) .

## <a name="syntax"></a>Sintaxis


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCertStore* \[ de\]
</dt> <dd>

Identificador de HCERTSTORE que se va a cerrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de **S \_ OK** indica que se ha realizado correctamente. Cualquier otro valor indica que se produjo un error en la operación.

## <a name="remarks"></a>Observaciones

Este método no libera el identificador HCERTSTORE contenido dentro de un objeto [**Store**](store.md) . Solo se debe usar para liberar un identificador de HCERTSTORE adquirido a través de la propiedad [**StoreHandle**](icertstore-storehandle.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




