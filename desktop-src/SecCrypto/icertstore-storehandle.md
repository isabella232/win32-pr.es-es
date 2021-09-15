---
description: Establece o recupera el identificador HCERTSTORE de un almacén de certificados.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: ICertStore::StoreHandle, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271028"
---
# <a name="icertstorestorehandle-property"></a>ICertStore::StoreHandle, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La **propiedad StoreHandle** establece o recupera el identificador HCERTSTORE de un almacén de certificados.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>Valor de propiedad

Identificador HCERTSTORE del almacén de certificados.

## <a name="error-codes"></a>Códigos de error

Si los métodos de acceso de **propiedad \_ ponen StoreHandle** y **get \_ StoreHandle** correctamente, devuelven S \_ OK.

Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="remarks"></a>Observaciones

Debe llamar al método [**CloseHandle**](icertstore-closehandle.md) o a la [**función CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) para liberar el contexto.

Si establece la propiedad **StoreHandle,** se restablece el estado de todo el objeto [**Store.**](store.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




