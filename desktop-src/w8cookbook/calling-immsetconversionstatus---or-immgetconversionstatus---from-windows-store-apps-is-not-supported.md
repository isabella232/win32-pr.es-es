---
title: No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde Windows store
description: No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde Windows store
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267423"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde Windows store

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde una aplicación Windows Store y puede provocar resultados inesperados.

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

 

 