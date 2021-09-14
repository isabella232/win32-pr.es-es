---
description: La estructura COMMCONFIG define la configuración de un recurso de comunicaciones, serie o de otro modo.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuración de recursos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164514"
---
# <a name="communications-resource-configuration"></a>Configuración de recursos de comunicaciones

La [**estructura COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) define la configuración de un recurso de comunicaciones, serie o de otro modo. El formato de la estructura varía en función del tipo de recurso de comunicaciones (el subtipo del proveedor). Los primeros miembros de estructura son comunes a todos los recursos de comunicaciones. Se definen miembros adicionales para subtipos de proveedor específicos. Los proveedores de servicios específicos también pueden extender la estructura **COMMCONFIG.**

Una aplicación puede obtener y establecer la configuración de un recurso de comunicaciones mediante las [**funciones GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) [**y SetCommConfig.**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) Cuando se abre, un recurso de comunicaciones se inicializa con la configuración predeterminada para su subtipo de proveedor. Para obtener y establecer la configuración predeterminada para un subtipo de proveedor, use las funciones [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) y [**SetDefaultCommConfig.**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)

Para solicitar al usuario información de configuración, use la [**función CommConfigDialog.**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) Esta función muestra un cuadro de diálogo definido por el proveedor de servicios y rellena una estructura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) basada en la entrada del usuario.

 

 



