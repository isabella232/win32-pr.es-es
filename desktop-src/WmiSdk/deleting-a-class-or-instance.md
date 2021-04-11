---
description: Después de terminar con una clase o una instancia, puede que desee eliminar esa clase o instancia de WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Eliminar una clase o una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276262"
---
# <a name="deleting-a-class-or-instance"></a>Eliminar una clase o una instancia

Después de terminar con una clase o una instancia, puede que desee eliminar esa clase o instancia de WMI. Al igual que otras tecnologías orientadas a objetos, puede eliminar objetos de clase o instancia para limpiar el espacio de nombres WMI y devolver recursos del sistema. Sin embargo, muchas clases e instancias en WMI son persistentes y se usan en una gran variedad de aplicaciones en un momento dado. por lo tanto, debe tener cuidado al eliminar una clase o instancia de WMI: la aplicación u otra aplicación probablemente necesitará la clase o instancia en una fecha posterior.

Eliminar una clase o una instancia es un procedimiento sencillo. Sin embargo, debido a la naturaleza permanente de una clase, probablemente no necesitará eliminar una clase a menudo. Por ejemplo, es poco probable que elimine la clase [**\_ DiskDrive de Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , porque es improbable que no tenga una unidad de disco en alguna parte de la empresa. En su lugar, es más probable que se elimine una instancia de una clase. Para obtener más información, consulte [eliminar una instancia](deleting-an-instance.md).

Aunque es poco frecuente, puede que le interese una vez que desee actualizar una clase que haya creado. Por ejemplo, podría crear una clase para representar una aplicación de otro fabricante. Si el software de terceros actualizara su software hasta el punto de que la clase ya no represente correctamente el software, es posible que tenga que eliminar la clase original. Para obtener más información, vea [eliminar una clase](deleting-a-class.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases de Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
