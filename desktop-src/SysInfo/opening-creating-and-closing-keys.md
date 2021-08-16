---
description: Para que una aplicación pueda agregar datos al Registro, debe crear o abrir una clave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Apertura, creación y cierre de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605d53a00506122c6350abd7f06e9166ed487de98c7910a3b7c3a913978492f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763967"
---
# <a name="opening-creating-and-closing-keys"></a>Apertura, creación y cierre de claves

Para que una aplicación pueda agregar datos al Registro, debe crear o abrir una clave. Para crear o abrir una clave, una aplicación siempre hace referencia a la clave como una subclave de una clave abierta actualmente. Las siguientes claves predefinidas siempre están abiertas: **HKEY \_ LOCAL \_ MACHINE**, **HKEY \_ CLASSES \_ ROOT**, **HKEY \_ USERS** y **HKEY CURRENT \_ \_ USER**. Una aplicación usa la [**función RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) para abrir una clave y la [**función RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) para crear una clave. Un árbol del Registro puede tener 512 niveles de profundidad. Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.

Una aplicación puede usar la [**función RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) para cerrar una clave y escribir los datos que contiene en el Registro. **RegCloseKey** no escribe necesariamente los datos en el Registro antes de devolverlos; la memoria caché puede tardar hasta varios segundos en vaciarse en el disco duro. Si una aplicación debe escribir explícitamente datos del Registro en el disco duro, puede usar la [**función RegFlushKey.**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) **Sin embargo, RegFlushKey** usa muchos recursos del sistema y solo debe llamarse cuando sea absolutamente necesario.

 

 



