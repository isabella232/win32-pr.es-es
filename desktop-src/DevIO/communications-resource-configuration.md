---
description: La estructura COMMCONFIG define la configuración de un recurso de comunicaciones, en serie o de otro tipo.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuración de recursos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153096"
---
# <a name="communications-resource-configuration"></a>Configuración de recursos de comunicaciones

La estructura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) define la configuración de un recurso de comunicaciones, en serie o de otro tipo. El formato de la estructura varía en función del tipo de recurso de comunicaciones (el subtipo de proveedor). Los primeros miembros de la estructura son comunes a todos los recursos de comunicaciones; los miembros adicionales se definen para los subtipos específicos del proveedor. Los proveedores de servicios concretos también pueden extender la estructura **COMMCONFIG** .

Una aplicación puede obtener y establecer la configuración de un recurso de comunicaciones mediante las funciones [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) y [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) . Cuando se abre, se inicializa un recurso de comunicaciones con la configuración predeterminada de su subtipo de proveedor. Para obtener y establecer la configuración predeterminada para un subtipo de proveedor, use las funciones [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) y [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .

Para solicitar al usuario información de configuración, utilice la función [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) . Esta función muestra un cuadro de diálogo definido por el proveedor de servicios y rellena una estructura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) en función de los datos proporcionados por el usuario.

 

 



