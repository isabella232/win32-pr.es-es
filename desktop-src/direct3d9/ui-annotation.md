---
description: Use esta anotación para asociar un parámetro de efecto a un control de interfaz de usuario en el entorno host. Esto permitirá que un usuario controle interactivamente un parámetro de efecto a través de la aplicación host.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Anotación de interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9e8816bb34ada52794694a2c6ae63ff663787a5db7419e9bf27a40f5aa0cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044073"
---
# <a name="ui-annotation"></a>Anotación de interfaz de usuario

Use esta anotación para asociar un parámetro de efecto a un control de interfaz de usuario en el entorno host. Esto permitirá que un usuario controle interactivamente un parámetro de efecto a través de la aplicación host.

DXSAS define un conjunto de controles estándar en términos del modelo de datos y el comportamiento básico que los autores pueden esperar de las aplicaciones host. La anotación de control se usa de la siguiente forma:


```
string SasUiControl = "ControlType";
```



where


```
ControlType
```



 es uno de los siguientes valores:



| ControlType | Descripción                                                                                                                                                                     | Tipo de datos interno                                                                                 | Anotaciones de propiedades de control                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Ninguno        | No se debe mostrar ningún control. Tenga en cuenta que un control es visible [si SasUiVisible](#sasuivisible) es True y el tipo de control es cualquier tipo distinto de None.                           | N/D                                                                                                | N/D                                                                                                          |
| Any         | Esto implica que no se solicita ningún control especial. El control presentado es el resultado del comportamiento definido por la aplicación.                                                         | N/D                                                                                                | N/D                                                                                                          |
| ColorPicker | Representa un valor de color como una muestra de color. El valor se empaqueta en los componentes XYZ del vector asociado. El componente W del vector asociado siempre se establece en uno. | float *N,* *donde N* es de 1 a 4 inclusive.                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| Dirección   | Vector de dirección.                                                                                                                                                             | float *N,* *donde N* es de 2 a 4 inclusive.                                                            | Ninguno                                                                                                         |
| FilePicker  | Cuadro de diálogo que permite al usuario examinar y seleccionar un archivo.                                                                                                                  | string                                                                                             | Ninguno                                                                                                         |
| ListPicker  | Lista de valores de cadena desde los que el usuario puede seleccionar una entrada. Los valores se generan a partir de la [anotación SasUiEnum.](#sasuienum)                                         | Matriz de cadenas junto con un valor entero que contiene el índice del valor de cadena seleccionado. | [SasUiEnum](#sasuienum)                                                                                      |
| Numeric     | Un conjunto de controles de entrada numéricos (por ejemplo, cuadros de texto).                                                                                                                         | float *M* x *N,* *donde M* y *N* son de 1 a 4 inclusive.                                               | [SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiStride](#sasuistride)                                    |
| Control deslizante      | Un conjunto de controles deslizantes.                                                                                                                                                               | float *M* x *N* donde *M* y *N* son de 1 a 4 inclusive                                                | [SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiSteps,](#sasuisteps) [SasUiStepsPower](#sasuistepspower) |
| String      | Cuadro de texto para editar contenido de cadena.                                                                                                                                         | string                                                                                             | Ninguno                                                                                                         |



 

Si el tipo de datos interno no es idéntico al tipo del parámetro asociado, la conversión se producirá cuando se transfieran datos del parámetro de aplicación host al parámetro de efecto.

El valor predeterminado es la cadena "None".

## <a name="ui-common-properties"></a>Propiedades comunes de la interfaz de usuario

### <a name="sasuidescription"></a>SasUiDescription

Use esta anotación para especificar una cadena para describir una herramienta. Esto se puede usar para elementos de la interfaz de usuario, como sugerencias de herramientas.


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

Use esta anotación para especificar una cadena para etiquetar cualquier control de interfaz de usuario.


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



Si se establece en True, la aplicación host debe mostrar un control de interfaz de usuario para editar el parámetro de efecto anotado. Si es false, no se muestra ninguna interfaz de usuario en la aplicación host.

Este es un ejemplo:


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



El valor predeterminado es True.

## <a name="ui-control-properties"></a>Propiedades del control de interfaz de usuario

Las anotaciones de propiedades de control son modificadores adicionales que ayudan a determinar cómo funciona un control determinado.

### <a name="sasuienum"></a>SasUiEnum

Esta anotación permite restringir el intervalo de valores de un control. La anotación contiene una cadena de valores delimitados por comas.

El valor predeterminado es una cadena vacía.

### <a name="sasuimax"></a>SasUiMax

Esta anotación especifica el valor máximo del parámetro asociado. Solo se puede asociar a un parámetro con tipo numérico. El valor máximo del parámetro se calculará realmente como:


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



PARAMETER \_ TYPE MAX es el valor máximo para el tipo utilizado por el parámetro \_ asociado. Esto significa que el valor del parámetro, teniendo en cuenta la anotación [SasUiMax,](#sasuimax) se calcula como:


```
ParameterValue = min(NewParameterValue, MaxValue);
```



El valor predeterminado es FLT \_ MAX, tal como se define en Math.h.

### <a name="sasuimin"></a>SasUiMin

Esta anotación especifica el valor mínimo del parámetro asociado. Solo se puede asociar a cualquier parámetro con tipo numérico. El valor mínimo del parámetro se calculará realmente como:


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



PARAMETER \_ TYPE MIN es el valor mínimo para el tipo utilizado por el parámetro \_ asociado. Esto significa que el valor del parámetro , teniendo en cuenta la anotación [SasUiMin](#sasuimin) se calcula como:


```
ParameterValue = max(NewParameterValue, MinValue);
```



El valor predeterminado es -FLT \_ MAX, tal como se define en Math.h.

### <a name="sasuisteps"></a>SasUiSteps

Esta anotación especifica el número de pasos que se pueden usar al incrementar o disminuir el valor del parámetro asociado. La anotación solo es significativa en un parámetro con tipo numérico. Cero especifica que la aplicación host elegirá un número razonable de pasos.

El valor predeterminado es 0.

### <a name="sasuistepspower"></a>SasUiStepsPower

Esta anotación especifica el exponente en la función de energía, que tiene el intervalo \[ 0,0f, 1,0f \] . Las aplicaciones host deben implementar el método siguiente al calcular los valores de parámetro:


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



El valor predeterminado es 1,0f.

### <a name="sasuistride"></a>SasUiStride

Esta anotación especifica el incremento que se debe usar al incrementar o disminuir este valor. A diferencia de [SasUiSteps,](#sasuisteps) [SasUiStride](#sasuistride) es útil con un control de número, por ejemplo, donde los datos están sin enlazar y el usuario prefiere incrementar el valor del parámetro por intervalo en lugar de por un número predefinido de pasos. Las aplicaciones host deben incrementar (o disminuir en función del comportamiento del control) por el valor de SasUiStride como se muestra a continuación:


```
ParameterValue = ParameterValue +/- SasUiStride
```



El valor predeterminado es 1,0f.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de anotaciones y semánticas estándar de DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



