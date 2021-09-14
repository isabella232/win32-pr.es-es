---
description: La propiedad MSINEWINSTANCE indica la instalación de una nueva instancia de un producto con transformaciones de instancia.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Propiedad MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074367"
---
# <a name="msinewinstance-property"></a>Propiedad MSINEWINSTANCE

La **propiedad MSINEWINSTANCE** indica la instalación de una nueva instancia de un producto con transformaciones de instancia. Esta propiedad admite varias instancias a través de transformaciones de cambio de código de producto. El valor de esta propiedad es 1. La presencia de esta propiedad en la línea de comandos requiere que la [**propiedad TRANSFORMS**](transforms.md) también esté presente. La primera transformación enumerada en **TRANSFORMS** debe ser una transformación de instancia. Para más información, consulte [Instalación de varias instancias de productos y revisiones.](installing-multiple-instances-of-products-and-patches.md)

Esta propiedad está disponible con el instalador que ejecuta un sistema en Windows Server 2003 o Windows XP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




