---
description: El enrutador de varios proveedores (MPR) llama a NPGetCaps para averiguar cuándo se iniciarán los proveedores de red (nIndex se establece en WNNC \_ START).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Invalidar el intervalo de tiempo de espera de MPR predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51c2c9db2fb892b7c2fc9646a9328fb9de4b7f9782ff5204ed261b16471ca4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921139"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Invalidar el intervalo de tiempo de espera de MPR predeterminado

El [*enrutador de varios*](../secgloss/m-gly.md) proveedores (MPR) llama a [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para averiguar cuándo se iniciarán los proveedores de red *(nIndex* se establece en WNNC \_ START). A continuación, el MPR espera el período de tiempo de espera más largo especificado por todos los proveedores de red antes de presentar la red consolidada al usuario. Si uno de los proveedores de red no sabe cuándo se iniciará, MPR usa un tiempo de espera predeterminado de 60 segundos para ese proveedor.

Si es necesario, el administrador puede invalidar el tiempo de espera predeterminado mediante la creación del siguiente tiempo de espera del Registro **\_ REG DWORD,** donde *n* es el intervalo de tiempo de espera en milisegundos:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*

El pseudocódigo siguiente muestra el flujo lógico completo para el control del tiempo de espera por parte del MPR.


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



 

 
