---
description: La presencia de la propiedad MSIINSTANCEGUID indica que un código de producto&\# 8211; el cambio de transformación se registra en el producto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propiedad MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679114"
---
# <a name="msiinstanceguid-property"></a>Propiedad MSIINSTANCEGUID

La presencia de la propiedad **MSIINSTANCEGUID** indica que se ha registrado un código de producto que cambia de transformación en el producto. El valor de la propiedad **MSIINSTANCEGUID** especifica qué instancia de un producto se va a usar para la instalación. La propiedad **MSIINSTANCEGUID** solo puede hacer referencia a un producto que ya se ha instalado con una transformación de instancia.

Las transformaciones de instancia son código de producto: cambiar las transformaciones disponibles con el instalador que se ejecuta en Windows Server 2003 o Windows XP. Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




