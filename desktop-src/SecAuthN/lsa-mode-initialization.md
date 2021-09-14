---
description: Cuando se inicia el sistema del equipo, la autoridad de seguridad local (LSA) carga automáticamente todos los archivos DLL del proveedor de compatibilidad de seguridad o del paquete de autenticación (SSP/AP) registrados en su espacio de proceso. En las ilustraciones siguientes se muestra el proceso de inicialización.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Inicialización del modo LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173505"
---
# <a name="lsa-mode-initialization"></a>Inicialización del modo LSA

Cuando se inicia el sistema del equipo, la autoridad de [](../secgloss/s-gly.md)seguridad [*local*](../secgloss/l-gly.md) (LSA) carga automáticamente todos los archivos DLL del paquete de autenticación del proveedor de compatibilidad de seguridad / [](../secgloss/a-gly.md) (SSP/AP) registrados en su espacio de proceso. En las ilustraciones siguientes se muestra el proceso de inicialización.

> [!Note]  
> "Kerberos" representa el SSP/AP de Microsoft [*Kerberos*](../secgloss/k-gly.md) y "Mi SSP/AP" representa un SSP/AP personalizado que contiene dos paquetes de seguridad personalizados.

 

![Inicialización del modo lsa](images/lsamode1.png)

Al iniciarse, el LSA llama a la función [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) en cada SSP/AP para obtener punteros a las funciones implementadas por cada paquete de seguridad en el archivo DLL. [](../secgloss/s-gly.md) Los punteros de función se pasan al LSA en una matriz de estructuras [**SECPKG \_ FUNCTION \_ TABLE.**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table)

![lsa llama a splsamodeinitialize para obtener punteros de función](images/lsamode2.png)

Después de recibir el conjunto de estructuras [**SECPKG \_ FUNCTION \_ TABLE,**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) el LSA llama a la función [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de cada paquete de seguridad. El LSA usa esta llamada de función para pasar a cada paquete de seguridad una estructura [**\_ SECPKG \_ FUNCTION \_ TABLE de LSA,**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) que contiene punteros a las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad. Además de almacenar los punteros a las funciones de compatibilidad de LSA, los paquetes de seguridad personalizados deben usar su implementación de la función **SpInitialize** para realizar cualquier procesamiento relacionado con la inicialización.

Para obtener una lista de las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad en modo LSA, vea Funciones de LSA llamadas por [SSP/AP.](authentication-functions.md)

Para obtener información sobre cómo registrar un archivo DLL de SSP/AP, vea Registrar archivos DLL [de SSP/AP.](registering-ssp-ap-dlls.md)

 

 
