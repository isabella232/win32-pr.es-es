---
description: Administración de combinaciones de energía
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Administración de combinaciones de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667210"
---
# <a name="power-scheme-management"></a>Administración de combinaciones de energía

Cada plan de energía se identifica de forma única mediante un **GUID**. Para enumerar todos los esquemas de energía disponibles, utilice la función [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) . **PowerEnumerate** también se puede usar para recuperar toda la configuración de energía de un esquema especificado.

El plan de energía que se usa actualmente en el sistema se conoce como plan de energía activo o plan. Para recuperar el **GUID** del plan activo, llame a la función [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) . Para cambiar el plan de energía activo, llame a la función [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .

Para crear un plan de energía, primero debe duplicar un esquema existente mediante la función [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , especificando el **GUID** del esquema en el que desea basar el nuevo esquema. Debe copiar uno de los esquemas integrados y modificar la configuración de energía según sus necesidades. Tenga en cuenta que al crear un plan de energía, no se actualiza automáticamente el plan de energía activo. Siempre debe llamar a [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) para actualizar el plan de energía activo. Los planes de energía existentes se pueden modificar y aplicar de la misma manera.

Para quitar un plan de energía, llame a la función [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .

> [!Note]  
> Para recuperar información adicional sobre el estado de energía del sistema, llame a la función [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Planes de energía](power-schemes.md)
</dt> </dl>

 

 



