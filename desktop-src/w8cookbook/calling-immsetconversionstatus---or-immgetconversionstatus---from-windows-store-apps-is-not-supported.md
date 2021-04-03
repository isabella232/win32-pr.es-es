---
title: No se admite la llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde aplicaciones de la tienda Windows
description: No se admite la llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde aplicaciones de la tienda Windows
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791920"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>No se admite la llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde aplicaciones de la tienda Windows

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8,1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

La llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde una aplicación de la tienda Windows no se admite y puede producir resultados inesperados.

## <a name="manifestations"></a>Manifestaciones

Al iniciarse la aplicación, el modo IME se establece en los valores predeterminados siguientes:



|          | Panel de entrada de software | Teclado de hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Activado                   | Off               |
| CHS, CHT | Activado                   | Activado                |



 

## <a name="solution"></a>Solución

Los desarrolladores pueden controlar el modo IME predeterminado especificando un valor de ámbito de entrada para el campo.

Cada IME determina el modo IME para un ámbito de entrada especificado. Los desarrolladores no pueden especificar el modo IME.

## <a name="resources"></a>Recursos

-   [InputScope (enumeración)](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 