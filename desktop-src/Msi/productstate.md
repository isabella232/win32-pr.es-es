---
description: El instalador establece la propiedad ProductState en el estado de instalación del producto durante la inicialización.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Propiedad ProductState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b4be53a1764d2277aec2b9acc50ae2a62ee7cb6687752466529c7ceabc689d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074665"
---
# <a name="productstate-property"></a>Propiedad ProductState

El instalador establece la **propiedad ProductState** en el estado de instalación del producto durante la inicialización. Esta propiedad se establece en uno de los siguientes tipos de datos INSTALLSTATE devueltos [**por MsiQueryProductState.**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)



| INSTALLSTATE             | Valor numérico | Estado de instalación del producto                   |
|--------------------------|---------------|-------------------------------------------------|
| INSTALLSTATE \_ UNKNOWN    | -1            | El producto no se anuncia ni se instala. |
| INSTALLSTATE \_ ANUNCIADO | 1             | El producto se anuncia pero no se instala.    |
| INSTALLSTATE \_ ABSENT     | 2             | El producto se instala para un usuario diferente.  |
| INSTALLSTATE \_ DEFAULT    | 5             | El producto se instala para el usuario actual.  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




