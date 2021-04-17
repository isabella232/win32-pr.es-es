---
description: Para que una aplicación pueda agregar datos al registro, debe crear o abrir una clave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Abrir, crear y cerrar claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666636"
---
# <a name="opening-creating-and-closing-keys"></a>Abrir, crear y cerrar claves

Para que una aplicación pueda agregar datos al registro, debe crear o abrir una clave. Para crear o abrir una clave, una aplicación siempre hace referencia a la clave como una subclave de una clave abierta actualmente. Las siguientes claves predefinidas siempre están abiertas **: HKEY \_ local \_ Machine**, **HKEY \_ classes \_ root**, **HKEY \_ users** y **HKEY \_ Current \_ User**. Una aplicación utiliza la función [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) para abrir una clave y la función [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) para crear una clave. Un árbol del registro puede tener un nivel de 512 niveles de profundidad. Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.

Una aplicación puede usar la función [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) para cerrar una clave y escribir los datos que contiene en el registro. **RegCloseKey** no escribe necesariamente los datos en el registro antes de devolver; la memoria caché puede tardar hasta varios segundos en vaciarse en el disco duro. Si una aplicación debe escribir explícitamente los datos del registro en el disco duro, puede usar la función [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) . Sin embargo, **RegFlushKey** utiliza muchos recursos del sistema y solo se debe llamar cuando sea absolutamente necesario.

 

 



