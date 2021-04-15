---
title: Modificador/backward_compat
description: El \_ modificador de compatibilidad/backward indica al compilador de MIDL que desactive algunas características avanzadas al generar código auxiliar de RPC/com.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676125"
---
# <a name="backward_compat-switch"></a>/backward ( \_ modificador compatible)

El \_ modificador de compatibilidad/backward indica al compilador de MIDL que desactive algunas características avanzadas al generar código auxiliar de RPC/com.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Opciones de conmutador

*tamaño de maybenull \_*<dl> Aplica el atributo [ \[ deshabilitar \_ \_ comprobación \] de coherencia](disable-consistence-check.md) a una compilación de MIDL completa.  
</dl>

*zeroout \_ alignmentgap*<dl> Desactiva el llenado de ceros en el búfer de serialización.  
</dl>

*Escape de BSTR \_ byvalue \_*<dl> Indica al compilador de MIDL que respete las secuencias de escape, como â € ̃ \\ nâ™ o â € ̃ \\ tÂ™ en BSTR.  
</dl>

*cadena \_ DefaultValue*<dl> Obliga al compilador de MIDL a convertir las cadenas de los atributos [**\[ DEFAULTVALUE \]**](defaultvalue.md) en Variant. VT \_ I4 Type antes de forzar el valor en el tipo correcto.  
</dl>

*\_WCHAR firmado \_ t*<dl> Indica a MIDL que trate el \_ tipo WCHAR t como firmado para la compatibilidad con Visual Basic.  
</dl>

## <a name="remarks"></a>Observaciones

-   *\_ tamaño de maybenull*: consulte \[ deshabilitar la \_ comprobación de coherencia \_ \] .
-   *zeroout \_ alignmentgap*: cuando se compilan pero con â € "Target NT60 o una versión posterior, MIDL creará códigos auxiliares que desconectan cualquier hueco de alineación entre miembros o una estructura en el búfer de conexión. El modificador de línea de comandos */backward \_ compat zeroout \_ ALIGNMENTGAP* dirige a MIDL para deshabilitar esta característica.

    En la estructura de ejemplo siguiente, el búfer de conexión contiene un intervalo de alineación de 7 bytes para alinear el miembro de hipertexto con 8 después del miembro de carácter. Con "NT60 de destino" o superior, MIDL dejará sin espacio a menos que se use el modificador.

    Archivo IDL:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Este modificador puede proporcionar una ligera mejora del rendimiento con aumentos potencialmente significativos en el riesgo de divulgación.

-   *BSTR \_ byvalue \_ Escaping*: de forma predeterminada, el COMpilador de MIDL no procesa secuencias de escape como â € ̃ \\ nÂ €™ o â € ̃ \\ tÂ €™ en constantes de cadena para la automatización OLE al convertir una constante de cadena en tipos VT \_ LPSTR o VT \_ LPWStr. Con esta opción de cambio de compatibilidad con versiones anteriores, se evalúan las secuencias de escape.
-   *String \_ DefaultValue*: obliga al compilador de MIDL a convertir las cadenas numéricas de los atributos [**\[ \] DefaultValue**](defaultvalue.md) en Variant. VT \_ I4 Type antes de forzar el valor en el tipo correcto. Esto puede dar lugar a la pérdida de precisión en algunos casos, por lo que no se recomienda esta opción de modificador.
-   *signed \_ WCHAR \_ t*: indica a MIDL que trate el \_ tipo WCHAR t como firmado para la compatibilidad con Visual Basic.

 

 




