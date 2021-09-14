---
description: Administración de esquemas de energía
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Administración de esquemas de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062849"
---
# <a name="power-scheme-management"></a>Administración de esquemas de energía

Cada esquema de energía se identifica de forma única mediante un **GUID.** Para enumerar todos los esquemas de energía disponibles, use la [**función PowerEnumerate.**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) **PowerEnumerate** también se puede usar para recuperar toda la configuración de energía para un esquema especificado.

El esquema de energía que se usa actualmente en el sistema se denomina esquema de energía activo o plan. Para recuperar el **GUID** del plan activo, llame a la [**función PowerGetActiveScheme.**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) Para cambiar el plan de energía activo, llame a la [**función PowerSetActiveScheme.**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme)

Para crear un esquema de energía, primero debe duplicar un esquema existente mediante la función [**PowerDuplicateScheme,**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) especificando el **GUID** del esquema en el que desea basar el nuevo esquema. Debe copiar uno de los esquemas integrados y modificar la configuración de energía según sus necesidades. Tenga en cuenta que la creación de un plan de energía no actualiza automáticamente el plan de energía activo. Siempre debe llamar a [**PowerSetActiveScheme para**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) actualizar el plan de energía activo. Los planes de energía existentes se pueden modificar y aplicar de la misma manera.

Para quitar un plan de energía, llame a la [**función PowerDeleteScheme.**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme)

> [!Note]  
> Para recuperar información adicional sobre el estado de energía del sistema, llame a la [**función CallNtPowerInformation.**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquemas de energía](power-schemes.md)
</dt> </dl>

 

 



