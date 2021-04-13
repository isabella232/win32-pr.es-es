---
description: Los scripts y las aplicaciones escritas para sistemas operativos de 32 bits deben seguir ejecutándose correctamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Proporcionar datos WMI en una plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543686"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>Proporcionar datos WMI en una plataforma de 64 bits

Los scripts y las aplicaciones escritas para sistemas operativos de 32 bits deben seguir ejecutándose correctamente. Si tiene un proveedor de 32 bits existente, puede evaluar si tiene que escribir una versión de 64 bits para la operación en paralelo. Por lo general, ambas versiones no son necesarias y la versión de 64 bits puede atender a clientes locales o remotos de 32 y 64 bits. Sin embargo, para el modo de compatibilidad de aplicaciones de 32 bits, use el proveedor de WMI de 32 bits existente en un sistema de 64 bits que se ejecute en el modo WOW64 de 32 bits.

En raras ocasiones, los proveedores de 32 bits y 64 bits deben ejecutarse en paralelo en sistemas de 64 bits. En este caso, la versión adecuada del proveedor que se carga depende de si el llamador es de 32 bits o de 64 bits y local o remoto. Un autor de llamada que usa las marcas de contexto del objeto de conexión, **\_ \_ ProviderArchitecture** y **\_ \_ RequiredArchitecture**, puede solicitar que WMI cargue un proveedor no predeterminado. Para obtener más información, consulte [obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).

En el caso inusual de que deba ejecutar los proveedores de 32 bits y 64 bits en paralelo, debe asegurarse de que los escenarios de instalación y desinstalación se controlan con cuidado. Esto se debe a que WMI solo tiene un [*repositorio*](gloss-w.md) y las versiones de 32 bits y 64 bits de [**mofcomp.exe**](mofcomp.md) colocan los datos en el mismo repositorio. no hay distinción entre un archivo. mof de 32 bits o de 64 bits. La reinstalación de una versión del proveedor no perjudicará: los archivos. mof se compilarán y las clases almacenadas en el repositorio. Sin embargo, una segunda desinstalación que elimina un espacio de nombres puede interferir con el funcionamiento del otro proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[Solicitar datos WMI en una plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Proporcionar datos a WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



