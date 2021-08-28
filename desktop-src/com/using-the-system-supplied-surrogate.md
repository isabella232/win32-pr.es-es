---
title: Uso de System-Supplied suplente
description: Uso de System-Supplied suplente
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0faec7c57f0e2010d0e817a4e44b81d65ad207371b591296bea2354307c7b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243435"
---
# <a name="using-the-system-supplied-surrogate"></a>Uso de System-Supplied suplente

Para usar el suplente proporcionado por el sistema para el servidor DLL, registre el archivo DLL especificando una cadena vacía o **NULL** para el [valor DllSurrogate](dllsurrogate.md) en el Registro. Cuando una solicitud de activación para un servidor DLL designado llega a COM, COM inicia el proceso suplente predeterminado y el archivo DLL solicitado (especificando el CLSID en la línea de comandos de inicio internamente) al mismo tiempo para evitar una llamada independiente. (Para obtener información sobre cómo ejecutar más de un servidor DLL en un proceso suplente, vea Uso compartido [de](surrogate-sharing.md)suplentes).

La implementación predeterminada del proceso suplente es un servidor pseudo-COM de estilo de modelo de subprocesos mixtos. Cuando se cargan varios servidores DLL en un único proceso suplente, este proceso garantiza que se cree una instancia de cada servidor DLL mediante el modelo de subprocesos especificado en el Registro para ese servidor. Todos los servidores de subprocesos libres cargados convivirán juntos en el apartamento multiproceso, mientras que cada servidor con subprocesos de apartamento residirá en un apartamento de un solo subproceso. Si un servidor DLL admite ambos modelos de subprocesos, COM elegirá multithreading.

Este proceso suplente se escribe para que COM controle la descarga de servidores DLL y la terminación del proceso suplente.

El suplente proporcionado por el sistema funcionará muy bien para la mayoría de los desarrolladores, además de ser muy fácil de usar. Sin embargo, los desarrolladores con consideraciones especiales pueden decidir que es necesario un suplente personalizado. Para obtener más información, [vea Escribir un suplente personalizado.](writing-a-custom-surrogate.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplentes de DLL](dll-surrogates.md)
</dt> </dl>

 

 




