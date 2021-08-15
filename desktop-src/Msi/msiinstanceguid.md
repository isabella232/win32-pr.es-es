---
description: La presencia de la propiedad MSIINSTANCEGUID indica que un código de producto&\# 8211;cambio de transformación se registra en el producto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propiedad MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f67f3f307eebecc25857411c25471ac3b39a97d48b48d6cc2894636c47f673b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679535"
---
# <a name="msiinstanceguid-property"></a>Propiedad MSIINSTANCEGUID

La presencia de la **propiedad MSIINSTANCEGUID** indica que se ha registrado en el producto una transformación de cambio de código de producto. El valor de la **propiedad MSIINSTANCEGUID** especifica qué instancia de un producto se va a usar para la instalación. La **propiedad MSIINSTANCEGUID** solo puede hacer referencia a un producto que ya se ha instalado con una transformación de instancia.

Las transformaciones de instancia son transformaciones de cambio de código de producto disponibles con el instalador que se ejecuta en Windows Server 2003 o Windows XP. Para obtener más información, [vea Instalación de varias instancias de productos y revisiones.](installing-multiple-instances-of-products-and-patches.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




