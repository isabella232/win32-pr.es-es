---
title: Uso de System-Supplied suplente
description: Uso de System-Supplied suplente
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973589"
---
# <a name="using-the-system-supplied-surrogate"></a>Uso de System-Supplied suplente

Para usar el suplente proporcionado por el sistema para el servidor DLL, registre el archivo DLL especificando una cadena vacía o **NULL** para el valor [DllSurrogate](dllsurrogate.md) en el Registro. Cuando una solicitud de activación para un servidor DLL designado llega a COM, COM inicia el proceso suplente predeterminado y el archivo DLL solicitado (especificando el CLSID en la línea de comandos de inicio internamente) al mismo tiempo para evitar una llamada independiente. (Para obtener información sobre cómo ejecutar más de un servidor DLL en un proceso suplente, vea Uso compartido [de](surrogate-sharing.md)suplentes).

La implementación predeterminada del proceso suplente es un servidor pseudo-COM de estilo de modelo de subprocesos mixtos. Cuando se cargan varios servidores DLL en un único proceso suplente, este proceso garantiza que se cree una instancia de cada servidor DLL mediante el modelo de subprocesos especificado en el Registro para ese servidor. Todos los servidores de subprocesos libres cargados residirán juntos en el apartamento multiproceso, mientras que cada servidor de subprocesos de apartamento residirá en un apartamento de un solo subproceso. Si un servidor DLL admite ambos modelos de subprocesos, COM elegirá multithreading.

Este proceso suplente se escribe para que COM controle tanto la descarga de servidores DLL como la finalización del proceso suplente.

El suplente proporcionado por el sistema funcionará muy bien para la mayoría de los desarrolladores, además de ser muy fácil de usar. Sin embargo, los desarrolladores con consideraciones especiales pueden decidir que es necesario un suplente personalizado. Para obtener más información, [vea Escribir un suplente personalizado.](writing-a-custom-surrogate.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplentes de DLL](dll-surrogates.md)
</dt> </dl>

 

 




