---
title: Obtener acceso a una vista del registro alternativa
description: De forma predeterminada, una aplicación de 32 bits que se ejecuta en WOW64 accede a la vista del Registro de 32 bits, y una aplicación de 64 bits accede a la vista del Registro de 64 bits.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- vistas del registro de la programación de Windows de 64 bits
- La programación de Windows de 64 bits de WOW64, vistas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105707504"
---
# <a name="accessing-an-alternate-registry-view"></a>Obtener acceso a una vista del registro alternativa

De forma predeterminada, una aplicación de 32 bits que se ejecuta en WOW64 accede a la vista del Registro de 32 bits, y una aplicación de 64 bits accede a la vista del Registro de 64 bits. Los siguientes marcadores permiten a las aplicaciones de 32 bits tener acceso a las claves redirigidas en la vista del registro de 64 bits y las aplicaciones de 64 bits para tener acceso a las claves redirigidas en la vista del registro de 32 bits. Estas marcas no tienen ningún efecto en las claves del registro compartidas. Para obtener más información, consulte [claves del registro afectadas por WOW64](shared-registry-keys.md).



| Nombre del marcador         | Value  | Descripción                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLAVE \_ WOW64 \_ 64KEY | 0x0100 | Obtenga acceso a una clave de 64 bits desde una aplicación de 32 bits o de 64 bits.                                                                                                                                                                                   |
| CLAVE \_ WOW64 \_ 32KEY | 0x0200 | Obtenga acceso a una clave de 32 bits desde una aplicación de 32 bits o de 64 bits.<br/>**Windows 10 en ARM:** Esto hace referencia a la vista del registro de ARM de 32 bits para los procesos ARM de 32 bits y la vista del registro x86 de 32 bits para los procesos de ARM64 de 32 bits x86 y de 64 bits. |



 

Estas marcas se pueden especificar en el parámetro *samDesired* de las siguientes funciones del registro:

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

\_Se puede especificar la clave WOW64 \_ 32KEY o la clave \_ WOW64 \_ 64KEY Si se especifican ambas marcas, se produce un ERROR en la función con un \_ parámetro no válido \_ .

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Si se especifican ambas marcas, el comportamiento de la función es indefinido.

No se puede usar la función [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) para tener acceso a una vista del registro alternativa.

A continuación se muestran los procedimientos recomendados para obtener acceso al registro desde una aplicación:

-   Una vez que la aplicación ha tenido acceso a una vista del registro alternativa mediante una de las marcas, todas las operaciones subsiguientes (crear, eliminar o abrir) en las claves del registro secundarias deben usar explícitamente la misma marca. De lo contrario, puede haber un comportamiento inesperado.
-   Para enumerar con precisión todas las claves en ambas vistas, realice la enumeración en dos pasos. El primer paso debe utilizar un identificador abierto con una de las marcas y el otro paso debe usar un identificador abierto con la otra marca.

> [!Note]  
> Las claves **Wow6432Node** y **WowAA32Node** están reservadas. Por compatibilidad, las aplicaciones no deben usar estas claves directamente.

 

Para obtener información sobre cómo obtener acceso a la vista del registro alternativa a través de WMI, consulte [solicitar datos WMI en una plataforma de 64 bits](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redirector del registro](registry-redirector.md)
</dt> <dt>

[Reflexión del registro](registry-reflection.md)
</dt> </dl>

 

