---
description: En las ventanas de 64 bits, las partes de las entradas del registro se almacenan por separado para las aplicaciones de la aplicación de 32 bits y de 64 y se asignan a vistas del registro lógico independientes mediante el redirector del registro y la reflexión del registro, ya que la versión de 64 bits de una aplicación puede usar diferentes claves y valores del registro que la versión de 32 bits. También hay claves del registro compartidas que no se redirigen ni reflejan.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Datos de aplicación de 32 bits y de 64 bits en el registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910014"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>Datos de aplicación de 32 bits y de 64 bits en el registro

En las ventanas de 64 bits, las partes de las entradas del registro se almacenan por separado para las aplicaciones de la aplicación de 32 bits y de 64 y se asignan a vistas del registro lógico independientes mediante el [redirector del registro](/windows/desktop/WinProg64/registry-redirector) y la [reflexión del registro](/windows/desktop/WinProg64/registry-reflection), ya que la versión de 64 bits de una aplicación puede usar diferentes claves y valores del registro que la versión de 32 bits. También hay [claves del registro compartidas](/windows/desktop/WinProg64/shared-registry-keys) que no se redirigen ni reflejan.

El elemento primario de cada nodo del registro de 64 bits es el nodo Image-Specific o no es. El redirector del registro dirige de forma transparente el acceso al registro de una aplicación al subnodo no es adecuado. El componente WOW64 crea automáticamente los subnodos de redirección en el árbol del registro con el nombre **Wow6432Node**. Como resultado, es esencial no nombrar cualquier clave del registro que cree **Wow6432Node**.

Las \_ marcas Key WOW64 \_ 64KEY y \_ 32KEY de clave WOW64 permiten el \_ acceso explícito a la vista del registro de 64 bits y la vista de 32 bits, respectivamente. Para obtener más información, vea [obtener acceso a una vista del registro alternativa](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).

Para deshabilitar y habilitar la reflexión del registro para una clave determinada, use las funciones [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) y [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) . Las aplicaciones solo deben deshabilitar la reflexión para las claves del registro que crean y no intentan deshabilitar la reflexión para las claves predefinidas como **HKEY \_ local \_ Machine** o **HKEY \_ Current \_ User**. Para determinar qué claves están en la lista de reflexión, utilice la función [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[redirector del registro](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[reflexión del registro](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
