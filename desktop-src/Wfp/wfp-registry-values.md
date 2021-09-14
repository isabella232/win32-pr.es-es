---
description: 'Los valores del Registro WFP se encuentran en la siguiente clave del Registro: HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valores del Registro WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249464"
---
# <a name="wfp-registry-values"></a>Valores del Registro WFP

\[Los valores del Registro WFP no se admiten a Windows Vista.\]

WFP usa varios valores del Registro para la configuración de personalización. Los valores del Registro WFP se encuentran en la siguiente clave del Registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

Los siguientes son los valores del Registro WFP.

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**
</dt> <dd>

Ubicación de la memoria caché. Debe ser una ruta de acceso local. El valor predeterminado es %systemroot% \\ system32 \\ dllcache.

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

Opciones de cuota. Este valor del Registro puede ser uno de los siguientes valores.



| Value                  | Significado                                                  |
|------------------------|----------------------------------------------------------|
| CUOTA DE SFC \_ \_ EN TODOS LOS \_ ARCHIVOS | El tamaño de la caché dll es ilimitado. Este es el valor predeterminado. |
| Otros valores           | Tamaño de la caché dll, en archivos.                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**
</dt> <dd>

Opciones de examen. Este valor del Registro puede ser uno de los siguientes valores.



| Value             | Significado                                                   |
|-------------------|-----------------------------------------------------------|
| SFC \_ SCAN \_ NORMAL | No digitalizar archivos protegidos durante el arranque. Este es el valor predeterminado. |
| SFC \_ SCAN \_ ALWAYS | Examinar archivos protegidos en cada arranque.                       |
| SFC \_ SCAN \_ ONCE   | Examinar archivos protegidos en el siguiente arranque.                    |



 

</dd> </dl>

 

 



