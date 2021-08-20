---
description: Lo usan las aplicaciones para enumerar objetos IWiaItem2 en la carpeta actual del árbol de elementos.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interfaz IEnumWiaItem2 (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: d9797a5b2349dd52c21204016d501fc2a34e4f6d2f71d7d4ee696aa208db01b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670208"
---
# <a name="ienumwiaitem2-interface"></a>Interfaz IEnumWiaItem2

Lo usan las aplicaciones para enumerar [**objetos IWiaItem2**](-wia-iwiaitem2.md) en la carpeta actual del árbol de elementos.

## <a name="members"></a>Miembros

La **interfaz IEnumWiaItem2** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumWiaItem2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumWiaItem2** tiene estos métodos.



| Método                                          | Descripción                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Clon**](-wia-ienumwiaitem2-clone.md)       | Crea una instancia adicional de la **interfaz IEnumWiaItem2** y le devuelve un puntero. <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | Devuelve el número de elementos almacenados por este enumerador. <br/>                                                          |
| [**Next**](-wia-ienumwiaitem2-next.md)         | Rellena una matriz de punteros a [**interfaces IWiaItem2.**](-wia-iwiaitem2.md)<br/>                                       |
| [**Restablecer**](-wia-ienumwiaitem2-reset.md)       | Restablece la referencia de enumeración al primer [**objeto IWiaItem2.**](-wia-iwiaitem2.md) <br/>                          |
| [**Omitir**](-wia-ienumwiaitem2-skip.md)         | Omite el número especificado de elementos durante una enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
