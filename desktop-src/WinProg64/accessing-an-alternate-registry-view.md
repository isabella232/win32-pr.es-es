---
title: Acceso a una vista alternativa del Registro
description: De forma predeterminada, una aplicación de 32 bits que se ejecuta en WOW64 accede a la vista del Registro de 32 bits, y una aplicación de 64 bits accede a la vista del Registro de 64 bits.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- Vistas del Registro de 64 bits Windows programación
- WOW64 64 bits de programación Windows , vistas del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1642de971a2342ab26114803689b8de21dd66194618a8db23f97170bc8da576a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859085"
---
# <a name="accessing-an-alternate-registry-view"></a>Acceso a una vista alternativa del Registro

De forma predeterminada, una aplicación de 32 bits que se ejecuta en WOW64 accede a la vista del Registro de 32 bits, y una aplicación de 64 bits accede a la vista del Registro de 64 bits. Las marcas siguientes permiten que las aplicaciones de 32 bits accedan a las claves redirigidas en la vista del Registro de 64 bits y a las aplicaciones de 64 bits para acceder a las claves redirigidas en la vista del Registro de 32 bits. Estas marcas no tienen ningún efecto en las claves compartidas del Registro. Para obtener más información, vea [Claves del Registro afectadas por WOW64.](shared-registry-keys.md)



| Nombre del marcador         | Value  | Descripción                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLAVE \_ WOW64 \_ 64KEY | 0x0100 | Acceda a una clave de 64 bits desde una aplicación de 32 o 64 bits.                                                                                                                                                                                   |
| CLAVE \_ WOW64 \_ 32KEY | 0x0200 | Acceda a una clave de 32 bits desde una aplicación de 32 o 64 bits.<br/>**Windows 10 en ARM:** Esto hace referencia a la vista del Registro de ARM de 32 bits para los procesos arm de 32 bits y la vista del Registro x86 de 32 bits para los procesos de 32 bits x86 y ARM64 de 64 bits. |



 

Estas marcas se pueden especificar en el parámetro *samDesired de* las siguientes funciones del Registro:

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

Se puede especificar KEY \_ WOW64 \_ 32KEY o KEY \_ WOW64 \_ 64KEY. Si se especifican ambas marcas, se produce un error en la función error \_ INVALID \_ PARAMETER.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Si se especifican ambas marcas, el comportamiento de la función es indefinido.

La [**función RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) no se puede usar para acceder a una vista alternativa del Registro.

Estos son los procedimientos recomendados al acceder al registro desde una aplicación:

-   Una vez que la aplicación ha accedido a una vista alternativa del Registro mediante una de las marcas, todas las operaciones posteriores (crear, eliminar o abrir) en las claves secundarias del Registro deben usar explícitamente la misma marca. De lo contrario, puede haber un comportamiento inesperado.
-   Para enumerar con precisión todas las claves de ambas vistas, realice la enumeración en dos pases. El primer paso debe usar un identificador abierto con una de las marcas y el otro debe usar un identificador abierto con la otra marca.

> [!Note]  
> Las **claves Wow6432Node** **y WowAA32Node** están reservadas. Por compatibilidad, las aplicaciones no deben usar estas claves directamente.

 

Para obtener información sobre el acceso a la vista alternativa del Registro a través de WMI, vea [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redirector del Registro](registry-redirector.md)
</dt> <dt>

[Reflexión del Registro](registry-reflection.md)
</dt> </dl>

 

