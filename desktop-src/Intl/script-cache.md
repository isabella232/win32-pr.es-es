---
description: Define una caché de métricas de fuentes uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171942"
---
# <a name="script_cache"></a>CACHÉ DE \_ SCRIPTS

Define una caché de métricas de fuentes uniscribe.


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>Observaciones

Se trata de una estructura opaca. La aplicación debe asignar y conservar una variable SCRIPT \_ CACHE para cada estilo de carácter utilizado. La variable debe inicializarse en **NULL.**

Muchas funciones de script toman una combinación de un identificador de contexto de dispositivo de hardware y una variable SCRIPT \_ CACHE. Uniscribe primero intenta acceder a los datos de fuente mediante la variable SCRIPT \_ CACHE. Solo inspecciona el contexto del dispositivo de hardware si los datos necesarios no están ya almacenados en caché.

El identificador de contexto del dispositivo de hardware se puede pasar a Uniscribe como **NULL.** Si los datos requeridos por Uniscribe ya están almacenados en caché, no se tiene acceso al contexto del dispositivo y la operación continúa con normalidad.

Si el contexto del dispositivo se pasa como **NULL** y Uniscribe necesita tener acceso a él por cualquier motivo, Uniscribe devuelve el código de error E \_ PENDING. Este código se devuelve rápidamente, lo que permite a la aplicación evitar llamadas [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) que requieren mucho tiempo.

## <a name="examples"></a>Ejemplos

El ejemplo siguiente se aplica a todas las funciones que toman una variable SCRIPT CACHE y \_ un identificador opcional en un contexto de dispositivo de hardware.


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Unscribe](uniscribe.md)
</dt> <dt>

[Estructuras de unidirección](uniscribe-structures.md)
</dt> <dt>

[Almacenamiento en caché](caching.md)
</dt> </dl>

 

 
