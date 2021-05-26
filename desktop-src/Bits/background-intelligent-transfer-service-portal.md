---
title: Servicio de transferencia inteligente en segundo plano
description: El Servicio de transferencia inteligente en segundo plano (BITS) transfiere archivos (descargas o cargas) entre un cliente y un servidor, y proporciona información sobre el progreso de las transferencias.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Servicio de transferencia inteligente en segundo plano
- Servicio de transferencia inteligente en segundo plano, página de inicio
- BITS (consulte Servicio de transferencia inteligente en segundo plano)
- descargar archivos BITS
- BITS de transferencia de archivos en segundo plano
- carga de archivos BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 9483e297e8b48ad6466846c7eceb8d53b57d3278
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424215"
---
# <a name="background-intelligent-transfer-service"></a>Servicio de transferencia inteligente en segundo plano

## <a name="purpose"></a>Propósito

Servicio de transferencia inteligente en segundo plano (BITS) los programadores y administradores del sistema usan para descargar o cargar archivos en servidores web HTTP y recursos compartidos de archivos SMB. BITS tendrá en cuenta el costo de la transferencia, así como el uso de la red para que el trabajo en primer plano del usuario tenga el menor impacto posible. BITS también controla las interupciones de red, pausando y reanudando automáticamente las transferencias, incluso después de un reinicio. BITS incluye cmdlets de PowerShell para crear y administrar transferencias, así como la utilidad de línea de comandos BitsAdmin.

> [!Note]  
> Windows puede usar BITS para descargar actualizaciones en el sistema local. Si es un usuario final que busca maneras de solucionar problemas de la instalación de BITS, consulte [Corrección de Windows Update problemas.](https://support.microsoft.com/help/10164/fix-windows-update-errors) 
 

## <a name="where-applicable"></a>Donde sea aplicable

Use BITS para las aplicaciones que necesitan:

-   Descargue o cargue archivos en un servidor web HTTP o REST o un servidor de archivos SMB.
-   Reanude automáticamente las transferencias de archivos después de que se desconecte la red y se reinicie el equipo.
-   Conserve la capacidad de respuesta de otras aplicaciones de red.
-   Tenga en cuenta el costo de red en, por ejemplo, las redes móviles.
-   Opcionalmente, trabaje con [BranchCache para](/windows-server/networking/branchcache/branchcache) optimizar el tráfico de red de área extensa (WAN).

## <a name="developer-audience"></a>Audiencia de desarrolladores

BITS es una interfaz COM diseñada para desarrolladores de C y C++ que también pueden usar los desarrolladores de .NET. Los desarrolladores de UWP deben usar la API [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) y no la API de BITS.

## <a name="bits-versions"></a>Versiones de BITS

Para obtener un historial completo de versiones e información sobre el sistema operativo anterior, vea [Novedades.](what-s-new.md)


## <a name="in-this-section"></a>En esta sección



| Tema                                                           | Descripción                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de BITS](about-bits.md)<br/>                         | Información general sobre BITS.<br/>                                                                                                                                      |
| [Uso de BITS](using-bits.md)<br/>                         | Guía de procedimientos para desarrollar clientes BITS que transfieren archivos entre un cliente y un servidor.<br/>                                                                        |
| [Referencia de BITS](bits-reference.md)<br/>                 | Información de referencia para las interfaces de programación de BITS. También contiene información sobre ejemplos, herramientas, configuración del servidor para trabajos de carga y el protocolo de carga.<br/> |
| [Procedimientos recomendados](best-practices-when-using-bits.md)<br/> | Información que se debe tener en cuenta al diseñar una aplicación que usa BITS.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Recursos adicionales

Los siguientes son recursos adicionales.


|    Recurso         |    Descripción                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL de referencia de .NET   | Para obtener información sobre el uso de BITS desde .NET mediante archivos DLL de referencia, vea Llamar a [BITS desde .NET mediante archivos DLL de referencia.](/windows/desktop/Bits/bits-dot-net)      |
| Contenedor de .NET   | Para otros contenedores de .NET para BITS, puede buscar [en nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) proyectos etiquetados con la etiqueta BITS.        |



 

 

