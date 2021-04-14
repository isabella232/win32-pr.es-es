---
description: El instalador establece la propiedad AFTERREBOOT en 1 después de un reinicio invocado por la acción ForceReboot. El instalador agrega AFTERREBOOT = 1 a la línea de comandos que se ejecuta inmediatamente después del reinicio.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propiedad AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653864"
---
# <a name="afterreboot-property"></a>Propiedad AFTERREBOOT

El instalador establece la propiedad **AFTERREBOOT** en 1 después de un reinicio invocado por la [acción ForceReboot](forcereboot-action.md). El instalador agrega AFTERREBOOT = 1 a la línea de comandos que se ejecuta inmediatamente después del reinicio.

## <a name="remarks"></a>Observaciones

La [acción ForceReboot](forcereboot-action.md) siempre debe usarse con una instrucción condicional de modo que el instalador desencadene un reinicio solo cuando sea necesario. Es posible que se requiera un reinicio si se ha reemplazado un archivo determinado o si se ha instalado un componente determinado. El caso es diferente para cada producto y podría ser necesaria una acción personalizada para determinar si es necesario un reinicio. Normalmente, la condición de la acción ForceReboot hace uso de la propiedad **AFTERREBOOT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 




