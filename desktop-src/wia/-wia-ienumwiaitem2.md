---
description: Lo usan las aplicaciones para enumerar los objetos IWiaItem2 en la carpeta actual del árbol de elementos.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interfaz IEnumWiaItem2 (WIA. h)
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
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652477"
---
# <a name="ienumwiaitem2-interface"></a>Interfaz IEnumWiaItem2

Lo usan las aplicaciones para enumerar los objetos [**IWiaItem2**](-wia-iwiaitem2.md) en la carpeta actual del árbol de elementos.

## <a name="members"></a>Miembros

La interfaz **IEnumWiaItem2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumWiaItem2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumWiaItem2** tiene estos métodos.



| Método                                          | Descripción                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Clonar**](-wia-ienumwiaitem2-clone.md)       | Crea una instancia adicional de la interfaz **IEnumWiaItem2** y le devuelve un puntero. <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | Devuelve el número de elementos almacenados por este enumerador. <br/>                                                          |
| [**Next**](-wia-ienumwiaitem2-next.md)         | Rellena una matriz de punteros a las interfaces de [**IWiaItem2**](-wia-iwiaitem2.md) .<br/>                                       |
| [**Reset**](-wia-ienumwiaitem2-reset.md)       | Restablece la referencia de enumeración al primer objeto [**IWiaItem2**](-wia-iwiaitem2.md) . <br/>                          |
| [**Omitir**](-wia-ienumwiaitem2-skip.md)         | Omite el número especificado de elementos durante una enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
