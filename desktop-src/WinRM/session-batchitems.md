---
title: Session.Batpropiedad chItems (WSManDisp. h)
description: Establece y obtiene el número de elementos de cada lote de enumeración.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad BatchItems
- Propiedad BatchItems Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, propiedad BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714614"
---
# <a name="sessionbatchitems-property"></a>Session.Batpropiedad chItems

Establece y obtiene el número de elementos de cada lote de enumeración. Este valor no se puede cambiar durante una enumeración. El proveedor de recursos puede establecer un límite.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Valor de propiedad

Especifica el número máximo de elementos devueltos para cada llamada de red subyacente al servicio. El valor predeterminado es 20.

## <a name="remarks"></a>Observaciones

Se trata de una característica de optimización que controla la frecuencia con que se realizan las llamadas de red entre el cliente y el servidor. Actualmente, solo se usa para las enumeraciones. Para obtener más información sobre la enumeración de recursos, vea [**enumerar**](session-enumerate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**De sesión**](session.md)
</dt> <dt>

[**Enumerar**](session-enumerate.md)
</dt> <dt>

[**Enumerador. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





