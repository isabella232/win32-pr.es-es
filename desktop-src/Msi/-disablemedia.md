---
description: El establecimiento de la propiedad DISABLEMEDIA evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto. Sin embargo, si la exploración está habilitada, es posible que un usuario siga explorando un origen de medios.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Propiedad DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670806"
---
# <a name="disablemedia-property"></a>Propiedad DISABLEMEDIA

El establecimiento de la propiedad [**DISABLEMEDIA**](disablemedia.md) evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto. Sin embargo, si la exploración está habilitada, es posible que un usuario siga explorando un origen de medios.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que la propiedad [**DISABLEMEDIA**](disablemedia.md) tiene un efecto diferente al establecimiento de la Directiva DISABLEMEDIA. La configuración de **DISABLEMEDIA** impide el registro de cualquier origen multimedia y esto también evita la primera instalación de una aplicación desde un origen de medios.

Para obtener más información acerca de cómo proteger los orígenes de medios de la [*aplicación administrada*](m-gly.md) frente a la exploración e instalación por parte de usuarios no administrativos, consulte [resistencia de origen](source-resiliency.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




