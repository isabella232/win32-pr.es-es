---
description: El instalador establece la propiedad ProductState en el estado de instalación del producto durante la inicialización.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: ProductState, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069760"
---
# <a name="productstate-property"></a>ProductState, propiedad

El instalador establece la **propiedad ProductState** en el estado de instalación del producto durante la inicialización. Esta propiedad se establece en uno de los siguientes tipos de datos INSTALLSTATE devueltos [**por MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).



| INSTALLSTATE             | Valor numérico | Estado de instalación del producto                   |
|--------------------------|---------------|-------------------------------------------------|
| INSTALLSTATE \_ UNKNOWN    | -1            | El producto no se anuncia ni se instala. |
| INSTALLSTATE \_ ANUNCIADO | 1             | El producto se anuncia pero no se instala.    |
| INSTALLSTATE \_ ABSENT     | 2             | El producto se instala para otro usuario.  |
| INSTALLSTATE \_ DEFAULT    | 5             | El producto se instala para el usuario actual.  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




