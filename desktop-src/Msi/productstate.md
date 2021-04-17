---
description: El instalador establece la propiedad ProductState en el estado de instalación del producto en la inicialización.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Propiedad ProductState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681304"
---
# <a name="productstate-property"></a>Propiedad ProductState

El instalador establece la propiedad **ProductState** en el estado de instalación del producto en la inicialización. Esta propiedad se establece en uno de los siguientes tipos de datos INSTALLSTATE devueltos por [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).



| INSTALLSTATE             | Valor numérico | Estado de la instalación del producto                   |
|--------------------------|---------------|-------------------------------------------------|
| INSTALLSTATE \_ desconocido    | -1            | El producto no se anuncia ni se instala. |
| INSTALLSTATE \_ anunciado | 1             | El producto se anuncia pero no se instala.    |
| INSTALLSTATE \_ ausente     | 2             | El producto se instala para un usuario diferente.  |
| INSTALLSTATE ( \_ valor predeterminado)    | 5             | El producto está instalado para el usuario actual.  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




