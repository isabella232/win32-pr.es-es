---
title: Propiedad WSMan. error (WSManDisp. h)
description: Obtiene información de error adicional, en una secuencia XML, para la llamada anterior a un método WSMan si Administración remota de Windows servicio no pudo crear un objeto de sesión, un objeto ConnectionOptions o un objeto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Error de la propiedad Administración remota de Windows
- Propiedad error Administración remota de Windows, objeto WSMan
- Administración remota de Windows de objeto WSMan, propiedad error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150327"
---
# <a name="wsmanerror-property"></a>WSMan. error (propiedad)

Obtiene información de error adicional, en una secuencia XML, para la llamada anterior a un método [**WSMan**](wsman.md) si administración remota de Windows servicio no pudo crear un objeto de [**sesión**](session.md) , un objeto [**ConnectionOptions**](connectionoptions.md) o un objeto [**ResourceLocator**](resourcelocator.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>Valor de propiedad

Representación XML de la información de error.

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

[**WSMan**](wsman.md)
</dt> </dl>

 

 





