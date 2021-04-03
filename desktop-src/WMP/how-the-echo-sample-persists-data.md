---
title: Cómo el ejemplo echo conserva los datos
description: Cómo el ejemplo echo conserva los datos
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df781754fd52639272850158187cb1258c081583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777095"
---
# <a name="how-the-echo-sample-persists-data"></a>Cómo el ejemplo echo conserva los datos

Cuando Windows Media Player habilita un complemento DSP, puede crear y destruir muchas instancias del objeto de complemento durante el transcurso de una sesión. El complemento necesita una manera de conservar los valores de propiedad entre las instancias. El código de ejemplo generado por el Asistente para complementos de Windows Media Player almacena estos valores en el registro y los recupera cuando se invoca la página de propiedades o cuando se crea una nueva instancia del complemento.

El código de ejemplo predeterminado en echo. h incluye dos constantes que almacenan la ruta de acceso predeterminada del registro y la cadena de nombre del factor de escala. Debe conservar la variable que especifica la ruta de acceso, pero elimine la línea que especifica el nombre del registro del factor de escala. A continuación, agregue el código siguiente para definir constantes para el tiempo de retraso y los nombres de propiedad de combinación húmeda en el registro. La sección finalizada debe aparecer de la siguiente manera:


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



Usará estas constantes cuando modifique los métodos de página de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades de ejemplo echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




