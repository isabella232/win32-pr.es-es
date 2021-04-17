---
description: Cuando se inicia el equipo, la autoridad de seguridad local (LSA) carga automáticamente todos los archivos dll registrados del proveedor de compatibilidad de seguridad (SSP/AP) en su espacio de proceso. En las ilustraciones siguientes se muestra el proceso de inicialización.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Inicialización del modo LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546347"
---
# <a name="lsa-mode-initialization"></a>Inicialización del modo LSA

Cuando se inicia el equipo, la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) carga automáticamente todos los archivos DLL del paquete de autenticación del [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) / [](../secgloss/a-gly.md) (SSP/AP) registrados en su espacio de proceso. En las ilustraciones siguientes se muestra el proceso de inicialización.

> [!Note]  
> "Kerberos" representa a Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP y "mi SSP/AP" representa un SSP/AP personalizado que contiene dos paquetes de seguridad personalizados.

 

![inicialización del modo LSA](images/lsamode1.png)

En el inicio, LSA llama a la función [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) en cada SSP/AP para obtener punteros a las funciones implementadas por cada [*paquete de seguridad*](../secgloss/s-gly.md) en el archivo dll. Los punteros de función se pasan a la LSA en una matriz de estructuras de [**\_ \_ tabla de la función SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .

![LSA llama a splsamodeinitialize para obtener punteros de función](images/lsamode2.png)

Después de recibir el conjunto de estructuras de [**\_ \_ tabla de funciones de SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , LSA llama a la función [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de cada paquete de seguridad. LSA usa esta llamada de función para pasar a cada paquete de seguridad una estructura de tabla de la [**\_ \_ función \_ LSA SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , que contiene punteros a las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad. Además de almacenar los punteros a las funciones de compatibilidad de LSA, los paquetes de seguridad personalizados deben usar su implementación de la función **SpInitialize** para realizar cualquier procesamiento relacionado con la inicialización.

Para obtener una lista de las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad de modo LSA, consulte [funciones de LSA llamadas por SSP/APS](authentication-functions.md).

Para obtener información acerca del registro de un archivo DLL SSP/AP, consulte [registro de dll de SSP/AP](registering-ssp-ap-dlls.md).

 

 
