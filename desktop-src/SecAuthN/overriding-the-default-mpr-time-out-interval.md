---
description: El enrutador de varios proveedores (MPR) llama a NPGetCaps para averiguar cuándo se iniciarán los proveedores de red (nIndex se establece en WNNC \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Reemplazar el intervalo de tiempo de espera predeterminado de MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002548"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Reemplazar el intervalo de tiempo de espera predeterminado de MPR

El [*enrutador de varios proveedores*](../secgloss/m-gly.md) (MPR) llama a [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para averiguar cuándo se iniciarán los proveedores de red (*NINDEX* se establece en WNNC \_ Start). A continuación, el MPR espera el período de tiempo de espera más largo especificado por todos los proveedores de red antes de presentar la red consolidada al usuario. Si uno de los proveedores de red no sabe cuándo se iniciará, MPR usará un tiempo de espera predeterminado de 60 segundos para ese proveedor.

Si es necesario, el administrador puede invalidar el tiempo de espera predeterminado creando el siguiente tiempo de espera del registro de **reg \_ DWORD** , donde *n* es el intervalo de tiempo de espera en milisegundos:

**HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*

En el siguiente pseudocódigo se muestra el flujo de lógica completo para el control de tiempo de espera del MPR.


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
