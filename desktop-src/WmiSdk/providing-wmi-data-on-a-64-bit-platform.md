---
description: Los scripts y aplicaciones escritos para sistemas operativos de 32 bits deben seguir funcionando correctamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Proporcionar datos WMI en una plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cb8a7e698723c6d4705a735591097fe7cf354db9684924d58f6b363c0ae6b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992645"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>Proporcionar datos WMI en una plataforma de 64 bits

Los scripts y aplicaciones escritos para sistemas operativos de 32 bits deben seguir funcionando correctamente. Si tiene un proveedor de 32 bits existente, puede evaluar si necesita escribir una versión de 64 bits para la operación en paralelo. Por lo general, ambas versiones no son necesarias y la versión de 64 bits puede ser compatible con clientes locales o remotos de 32 y 64 bits. Sin embargo, para el modo de compatibilidad de aplicaciones de 32 bits, use el proveedor WMI de 32 bits existente en un sistema de 64 bits que se ejecute en el modo WOW64 de 32 bits.

En raras situaciones, los proveedores de 32 y 64 bits deben ejecutarse en paralelo en sistemas de 64 bits. En este caso, la versión adecuada del proveedor que se carga depende de si el autor de la llamada es de 32 o 64 bits y local o remoto. Un llamador que usa las marcas de contexto del objeto de **\_ \_ conexión, ProviderArchitecture** y **\_ \_ RequiredArchitecture**, puede solicitar que WMI cargue un proveedor no predeterminado. Para obtener más información, vea Obtener y proporcionar datos en un equipo [de 64 bits.](getting-and-providing-data-on-a-64-bit-computer.md)

En el caso inusual de que debe ejecutar los proveedores de 32 y 64 bits en paralelo, debe asegurarse de que los escenarios de instalación y desinstalación se administran cuidadosamente. Esto se debe a [](gloss-w.md) que WMI solo tiene un repositorio y las versiones de 32 y 64 bits de [**mofcomp.exe**](mofcomp.md) colocar los datos en el mismo repositorio; no hay ninguna distinción entre un archivo .mof de 32 o 64 bits. La reinstalación de una versión del proveedor no hará daño: los archivos .mof se compilarán y las clases se almacenarán en el repositorio. Sin embargo, una segunda desinstalación que elimina un espacio de nombres puede interferir con el funcionamiento del otro proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[Solicitud de datos WMI en una plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Proporcionar datos a WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



