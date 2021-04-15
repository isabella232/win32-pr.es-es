---
title: Atributo WM/InitialKey
description: El atributo WM/InitialKey es la clave inicial de la música.
ms.assetid: 1458f1a2-3d46-4491-8b89-731276d7c024
keywords:
- Media Player de Windows de atributos de WM/InitialKey
topic_type:
- apiref
api_name:
- WM/InitialKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dd4daeabe2971615518b0a3cf37223a4c623c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708718"
---
# <a name="wminitialkey-attribute"></a>Atributo WM/InitialKey

El atributo **WM/InitialKey** es la clave inicial de la música.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMInitialKey.

**InitialKey** es un alias para este atributo.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





