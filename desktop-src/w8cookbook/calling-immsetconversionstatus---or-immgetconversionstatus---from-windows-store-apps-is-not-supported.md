---
title: No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde aplicaciones de la Tienda Windows
description: No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde aplicaciones de la Tienda Windows
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443155"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde aplicaciones de la Tienda Windows

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde una aplicación de la Tienda Windows y puede provocar resultados inesperados.

## <a name="manifestations"></a>Manifestaciones

Al iniciar la aplicación, el modo IME se establece en los valores predeterminados siguientes:



| &nbsp;   | Panel de entrada de software | Teclado de hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Activado                   | Desactivado               |
| CHS, CHT | Activado                   | Activado                |



 

## <a name="solution"></a>Solución

Los desarrolladores pueden controlar el modo IME predeterminado especificando un valor de ámbito de entrada para el campo.

Cada IME determina el modo IME para un ámbito de entrada especificado. Los desarrolladores no pueden especificar el modo IME.

## <a name="resources"></a>Recursos

-   [Enumeración InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 