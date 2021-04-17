---
description: La herramienta MFTrace puede leer un archivo de configuración XML que especifica uno o más proveedores de seguimiento.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Archivo de configuración MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652551"
---
# <a name="mftrace-configuration-file"></a>Archivo de configuración MFTrace

La herramienta [MFTrace](mftrace.md) puede leer un archivo de configuración XML que especifica uno o más proveedores de seguimiento.

El elemento [**providers**](providers.md) es el elemento raíz del archivo de configuración.

## <a name="in-this-section"></a>En esta sección

-   [**palabra clave**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**presta**](provider.md)
-   [**providers**](providers.md)

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

 

 



