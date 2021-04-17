---
description: 'Los valores del registro de WFP se encuentran en la siguiente clave del registro: HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valores del registro de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668441"
---
# <a name="wfp-registry-values"></a>Valores del registro de WFP

\[Los valores del registro de WFP no se admiten en Windows Vista.\]

WFP usa varios valores del registro para la configuración de personalización. Los valores del registro de WFP se encuentran en la siguiente clave del registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

Estos son los valores del registro de WFP.

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**
</dt> <dd>

Ubicación de la memoria caché. Debe ser una ruta de acceso local. El valor predeterminado es% SystemRoot% \\ system32 \\ dllcache.

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

Opciones de cuota. Este valor del registro puede ser uno de los siguientes valores.



| Value                  | Significado                                                  |
|------------------------|----------------------------------------------------------|
| \_ \_ todos \_ los archivos de cuota de SFC | El tamaño de la caché de DLL es ilimitado. Este es el valor predeterminado. |
| Otros valores           | Tamaño de la caché de DLL, en archivos.                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**
</dt> <dd>

Opciones de examen. Este valor del registro puede ser uno de los siguientes valores.



| Value             | Significado                                                   |
|-------------------|-----------------------------------------------------------|
| examen de SFC \_ \_ normal | No examinar archivos protegidos en el arranque. Este es el valor predeterminado. |
| detección de SFC \_ \_ siempre | Examinar los archivos protegidos en cada arranque.                       |
| \_examinar SFC \_ una vez   | Examinar los archivos protegidos en el siguiente arranque.                    |



 

</dd> </dl>

 

 



