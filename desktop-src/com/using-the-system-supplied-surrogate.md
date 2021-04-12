---
title: Usar el suplente System-Supplied
description: Usar el suplente System-Supplied
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357723"
---
# <a name="using-the-system-supplied-surrogate"></a>Usar el suplente System-Supplied

Para usar el suplente proporcionado por el sistema para el servidor DLL, registre el archivo DLL especificando una cadena vacía o **null** para el valor [DllSurrogate](dllsurrogate.md) en el registro. Cuando una solicitud de activación para un servidor DLL, por lo que se trata de COM, COM inicia el proceso suplente predeterminado y el archivo DLL solicitado (especificando el CLSID en la línea de comandos de inicio internamente) al mismo tiempo para evitar una llamada independiente. (Para obtener información sobre cómo ejecutar más de un servidor DLL en un proceso suplente, vea [uso compartido de suplentes](surrogate-sharing.md)).

La implementación predeterminada del proceso suplente es un servidor pseudo-COM de estilo de modelo de subprocesos mixtos. Cuando se cargan varios servidores DLL en un único proceso suplente, este proceso garantiza que se crea una instancia de cada servidor DLL utilizando el modelo de subprocesos especificado en el registro para ese servidor. Todos los servidores de subprocesos libres cargados residirán juntos en el apartamento multiproceso, mientras que cada servidor de subprocesos de Apartamento residirá en un contenedor uniproceso. Si un servidor DLL admite ambos modelos de subprocesos, COM elegirá multithreading.

Este proceso suplente se escribe para que COM controle tanto la descarga de los servidores DLL como la terminación del proceso suplente.

El suplente proporcionado por el sistema funcionará muy bien para la mayoría de los desarrolladores, así como para que sea muy fácil de usar. Sin embargo, los desarrolladores con consideraciones especiales pueden decidir que es necesario un suplente personalizado. Para obtener más información, consulte [Writing a Custom suplente](writing-a-custom-surrogate.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplentes DLL](dll-surrogates.md)
</dt> </dl>

 

 




