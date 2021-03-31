---
description: Use esta anotación para asociar un parámetro de efecto a un control de IU en el entorno de host. Esto permitirá a un usuario controlar interactivamente un parámetro de efecto a través de la aplicación host.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Anotación de interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495761"
---
# <a name="ui-annotation"></a>Anotación de interfaz de usuario

Use esta anotación para asociar un parámetro de efecto a un control de IU en el entorno de host. Esto permitirá a un usuario controlar interactivamente un parámetro de efecto a través de la aplicación host.

DXSAS define un conjunto de controles estándar en términos del modelo de datos y el comportamiento básico que los autores de efectos pueden esperar de las aplicaciones host. La anotación de control se usa de la siguiente manera:


```
string SasUiControl = "ControlType";
```



where


```
ControlType
```



es uno de los siguientes:



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| ControlType | Descripción                                                                                                                                                                     | Tipo de datos interno                                                                                 | Anotaciones de propiedades de control                                                                                 |
| None        | No debe mostrarse ningún control. Tenga en cuenta que un control está visible si [SasUiVisible](#sasuivisible) es true y el tipo de control es cualquier tipo que no sea ninguno.                           | N/D                                                                                                | N/D                                                                                                          |
| Any         | Esto implica que no se solicita ningún control especial. El control presentado es el resultado del comportamiento definido por la aplicación.                                                         | N/D                                                                                                | N/D                                                                                                          |
| ColorPicker | Representa un valor de color como una muestra de color. El valor se empaqueta en los componentes XYZ del vector asociado. El componente W del vector asociado siempre se establece en uno. | Float *n* , donde *N* es de 1 a 4, ambos inclusive.                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| Dirección   | Vector de dirección.                                                                                                                                                             | Float *n* , donde *N* es de 2 a 4, ambos inclusive.                                                            | None                                                                                                         |
| FilePicker  | Cuadro de diálogo que permite al usuario examinar y seleccionar un archivo.                                                                                                                  | string                                                                                             | None                                                                                                         |
| ListPicker  | Una lista de valores de cadena de la que el usuario puede seleccionar una entrada. Los valores se generan a partir de la anotación [SasUiEnum](#sasuienum) .                                         | Matriz de cadenas junto con un valor entero que contiene el índice del valor de cadena seleccionado. | [SasUiEnum](#sasuienum)                                                                                      |
| Numeric     | Conjunto de controles numéricos de entrada (como cuadros de texto).                                                                                                                         | Float *m* x *N* donde *M* y *N* son de 1 a 4, ambos inclusive.                                               | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)                                    |
| Control deslizante      | Un conjunto de controles deslizantes.                                                                                                                                                               | Float *m* x *N* donde *M* y *N* están entre 1 y 4, ambos incluidos                                                | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower) |
| String      | Cuadro de texto para editar el contenido de la cadena.                                                                                                                                         | string                                                                                             | None                                                                                                         |



 

Si el tipo de datos interno no es idéntico al tipo del parámetro asociado, la conversión se realizará cuando se transfieran los datos desde el parámetro de la aplicación host al parámetro de efecto.

El valor predeterminado es la cadena "none".

## <a name="ui-common-properties"></a>Propiedades comunes de la interfaz de usuario

### <a name="sasuidescription"></a>SasUiDescription

Use esta anotación para especificar una cadena que describa una herramienta. Se puede usar para elementos de la interfaz de usuario como la información sobre herramientas.


```
string SasUiDescription = "descriptive string";
```



Por ejemplo:


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



El valor predeterminado es una cadena vacía.

### <a name="sasuilabel"></a>SasUiLabel

Use esta anotación para especificar una cadena que etiquete cualquier control de IU.


```
string SasUiLabel = "some label;
```



Este es un ejemplo:


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



El valor predeterminado es una cadena vacía.

### <a name="sasuivisible"></a>SasUiVisible

Use esta anotación para especificar si el parámetro asociado se debe mostrar al usuario.


```
bool SasUiVisible = false;
```



Si se establece en true, la aplicación host debe mostrar un control de interfaz de usuario para editar el parámetro de efecto anotado. Si es false, no se muestra ninguna interfaz de usuario en la aplicación host.

Este es un ejemplo:


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



El valor predeterminado es True.

## <a name="ui-control-properties"></a>Propiedades de control de IU

Las anotaciones de propiedades de control son modificadores adicionales que ayudan a determinar cómo funciona un control determinado.

### <a name="sasuienum"></a>SasUiEnum

Esta anotación le permite restringir el intervalo de valores de un control. La anotación contiene una cadena de valores delimitada por comas.

El valor predeterminado es una cadena vacía.

### <a name="sasuimax"></a>SasUiMax

Esta anotación especifica el valor máximo del parámetro asociado. Solo se puede asociar con un parámetro con tipo numérico. El valor máximo del parámetro se calculará realmente como:


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



El \_ tipo \_ de parámetro Max es el valor máximo para el tipo utilizado por el parámetro asociado. Esto significa que el valor del parámetro, teniendo en cuenta la anotación [SasUiMax](#sasuimax) se calcula como:


```
ParameterValue = min(NewParameterValue, MaxValue);
```



El valor predeterminado es FLT \_ máx, tal y como se define en Math. h.

### <a name="sasuimin"></a>SasUiMin

Esta anotación especifica el valor mínimo del parámetro asociado. Solo se puede asociar a cualquier parámetro con tipo numérico. El valor mínimo del parámetro se calculará realmente como:


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



El \_ tipo \_ de parámetro min es el valor mínimo para el tipo utilizado por el parámetro asociado. Esto significa que el valor del parámetro, teniendo en cuenta la anotación [SasUiMin](#sasuimin) se calcula como:


```
ParameterValue = max(NewParameterValue, MinValue);
```



El valor predeterminado es-FLT \_ Max tal y como se define en Math. h.

### <a name="sasuisteps"></a>SasUiSteps

Esta anotación especifica el número de pasos que se pueden utilizar al aumentar o reducir el valor del parámetro asociado. La anotación solo es significativa en un parámetro con tipo numérico. Cero especifica que la aplicación host elegirá un número razonable de pasos.

El valor predeterminado es 0.

### <a name="sasuistepspower"></a>SasUiStepsPower

Esta anotación especifica el exponente de la función Power, que tiene el intervalo \[ 0.0 f, 1.0 f \] . Las aplicaciones host deben implementar el método siguiente al calcular los valores de parámetro:


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



El valor predeterminado es 1.0 f.

### <a name="sasuistride"></a>SasUiStride

Esta anotación especifica el incremento que se debe usar al incrementar o reducir este valor. A diferencia de [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) es útil con un control de número, por ejemplo, donde los datos están sin enlazar y el usuario aumentaría el valor del parámetro por STRIDE, en lugar de por un número predefinido de pasos. Las aplicaciones host deben incrementar (o disminuir en función del comportamiento del control) el valor de SasUiStride como se indica a continuación:


```
ParameterValue = ParameterValue +/- SasUiStride
```



El valor predeterminado es 1.0 f.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de las anotaciones y semánticas estándar de DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



