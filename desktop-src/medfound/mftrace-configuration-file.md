---
description: La herramienta MFTrace puede leer un archivo de configuración XML que especifica uno o varios proveedores de seguimiento.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Archivo de configuración de MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60969d52405b5aeeb768710d35751d9ea2cab40ca60a7d85a4da1bc1b0c65468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871942"
---
# <a name="mftrace-configuration-file"></a>Archivo de configuración de MFTrace

La [herramienta MFTrace](mftrace.md) puede leer un archivo de configuración XML que especifica uno o varios proveedores de seguimiento.

El [**elemento providers**](providers.md) es el elemento raíz del archivo de configuración.

## <a name="in-this-section"></a>En esta sección

-   [**Palabra clave**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**Proveedor**](provider.md)
-   [**Proveedores**](providers.md)

## <a name="example"></a>Ejemplo

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 



