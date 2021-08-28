---
title: /backward_compat Switch
description: El modificador /backward compat dirige al compilador midl a desactivar algunas características avanzadas al \_ generar código auxiliar RPC/COM.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd412bdabe4255a9a4538503b29ddf5681265ce5e16c81d3d5fc2484eb6c9675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086395"
---
# <a name="backward_compat-switch"></a>/backward \_ compat Switch

El modificador /backward compat dirige al compilador midl a desactivar algunas características avanzadas al \_ generar código auxiliar RPC/COM.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Cambiar opciones

*maybenull \_ sizeis*<dl> Aplica el atributo [ \[ disable consistency \_ \_ check \] ](disable-consistence-check.md) a una compilación MIDL completa.  
</dl>

*alineación \_ de cerosgap*<dl> Desactiva la puesta a cero de espacios en el búfer serializado.  
</dl>

*BSTR \_ por escape de \_ valores*<dl> Dirige al compilador MIDL a respetar secuencias de escape, como â€ \\ nâ€™ o â€ â€ \\ tâ€™ en BSTR.  
</dl>

*string \_ defaultvalue*<dl> Fuerza al compilador MIDL a convertir cadenas en [**\[ atributos de valor \]**](defaultvalue.md) predeterminado en VARIANT. Tipo \_ VT I4 antes de convertir el valor en el tipo correcto.  
</dl>

*signed \_ wchar \_ t*<dl> Dirige a MIDL para tratar el tipo wchar \_ t como firmado por compatibilidad con Visual Basic.  
</dl>

## <a name="remarks"></a>Comentarios

-   *maybenull \_ sizeis:* consulte \[ deshabilitar la comprobación de \_ \_ \] coherencia.
-   *\_ alignmentgap zeroout:* cuando los IDL se compilan con nt60 de destino o superior, MIDL creará códigos auxiliares que ceron las brechas de alineación entre los miembros o una estructura en el búfer de conexión. El modificador de línea de *comandos /backward \_ compat zeroout \_ alignmentgap* dirige MIDL para deshabilitar esta característica.

    En la estructura de ejemplo siguiente, el búfer de conexión contiene un intervalo de alineación de 7 bytes para alinear el miembro hyper con 8 después del miembro char. Con â€"target NT60 o superior, MIDL pondrá a cero esa brecha a menos que se utilice el modificador.

    Archivo IDL:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Este cambio puede proporcionar una ligera mejora del rendimiento con aumentos potencialmente significativos en el riesgo de divulgación.

-   Escape de BSTR por valor: de forma predeterminada, el compilador MIDL no procesa secuencias de escape como â€ miento nâ€™ o â€ omisión de ™ en constantes de cadena para OLE Automation al convertir una constante de cadena a tipos VT LPSTR o *\_ \_* \\ VT \\ \_ \_ LPWSTR. Con esta opción de modificador de compatibilidad con versiones anteriores, se evalúan las secuencias de escape.
-   *string \_ defaultvalue:* fuerza al compilador MIDL a convertir cadenas numéricas en [**\[ atributos defaultvalue \]**](defaultvalue.md) en VARIANT. Tipo \_ VT I4 antes de convertir el valor en el tipo correcto. Esto puede provocar la pérdida de precisión en algunos casos, por lo que no se recomienda esta opción de modificador.
-   *signed \_ wchar \_ t:* hace que MIDL trate el tipo wchar t como firmado por compatibilidad \_ con Visual Basic.

 

 




