---
description: El instalador establece la propiedad AFTERREBOOT en 1 después de un reinicio invocado por la acción ForceReboot. El instalador agrega AFTERREBOOT=1 a la línea de comandos que se ejecuta inmediatamente después del reinicio.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propiedad AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8fb80a3d8ff167f93aab6c95fc3eadb8b5312daf9d2a2856f01cb7d01ee383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145918"
---
# <a name="afterreboot-property"></a>Propiedad AFTERREBOOT

El instalador establece la **propiedad AFTERREBOOT** en 1 después de un reinicio invocado por la [acción ForceReboot](forcereboot-action.md). El instalador agrega AFTERREBOOT=1 a la línea de comandos que se ejecuta inmediatamente después del reinicio.

## <a name="remarks"></a>Comentarios

La [acción ForceReboot siempre](forcereboot-action.md) debe usarse con una instrucción condicional de modo que el instalador desencadene un reinicio solo cuando sea necesario. Es posible que sea necesario reiniciar si se ha reemplazado un archivo determinado o si se ha instalado un componente determinado. El caso es diferente para cada producto y es posible que sea necesaria una acción personalizada para determinar si se necesita un reinicio. La condición de la acción ForceReboot normalmente usa la **propiedad AFTERREBOOT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 




