---
title: Cómo conserva los datos el ejemplo de eco
description: Cómo conserva los datos el ejemplo de eco
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- Reproductor de Windows Media complementos, páginas de propiedades de ejemplo de eco
- complementos, páginas de propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, páginas de propiedades de ejemplo de eco
- Complementos de DSP, páginas de propiedades de ejemplo de Eco
- Ejemplo de complemento DSP de eco, páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df781754fd52639272850158187cb1258c081583
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476234"
---
# <a name="how-the-echo-sample-persists-data"></a>Cómo conserva los datos el ejemplo de eco

Cuando Reproductor de Windows Media un complemento DSP, puede crear y destruir muchas instancias del objeto de complemento durante el transcurso de una sesión. El complemento necesita una manera de conservar sus valores de propiedad entre instancias. El código de ejemplo generado por el Asistente para complementos de Reproductor de Windows Media almacena estos valores en el Registro y los recupera cuando se invoca la página de propiedades o cuando se crea una nueva instancia del complemento.

El código de ejemplo predeterminado de Echo.h incluye dos constantes que almacenan la ruta de acceso del Registro predeterminada y la cadena de nombre del factor de escala. Debe mantener la variable que especifica la ruta de acceso, pero eliminar la línea que especifica el nombre del registro del factor de escala. A continuación, agregue el código siguiente para definir constantes para el tiempo de retraso y los nombres de propiedad de mezcla con mezcla en el registro. La sección finalizada debe aparecer como sigue:


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



Usará estas constantes al modificar los métodos de página de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




