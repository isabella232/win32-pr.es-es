---
title: Método External.NavigateTaskPaneURL
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Método External.NavigateTaskPaneURL
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Método NavigateTaskPaneURL Reproductor de Windows Media
- Método NavigateTaskPaneURL Reproductor de Windows Media , clase External
- Clase externa Reproductor de Windows Media método , NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebcf8d799452a9966355f644f00ac5c4aecc4c066374254e8e580431b756b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649035"
---
# <a name="externalnavigatetaskpaneurl-method"></a>Método External.NavigateTaskPaneURL

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método NavigateTaskPaneURL** abre una página web en el panel de tareas especificado y cambia el foco al panel especificado.

## <a name="syntax"></a>Sintaxis


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKeyName* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre de clave para el almacén en línea. (necesario)

</dd> <dt>

*bstrTaskPane* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del panel de tareas en el que se abre la página web. (necesario)

</dd> <dt>

*bstrParams* \[ En\]
</dt> <dd>

**Cadena** que contiene los parámetros de cadena de consulta que se anexarán a la dirección URL especificada por el **elemento Navigate** del documento ServiceInfo. (opcional).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Navegar a un panel que la tienda en línea no admite puede hacer que cambie la tienda en línea actual.

El valor especificado para *bstrParams* solo es válido cuando se llama a **NavigateTaskPaneURL** desde páginas web proporcionadas por la tienda en línea.

En la tabla siguiente se enumeran los valores válidos *para bstrTaskPane* y el panel de tareas asociado para cada uno.



| Value            | Panel de tareas                      |
|------------------|--------------------------------|
| **ServiceTask1** | Primer panel de tareas de la tienda en línea.  |
| **ServiceTask2** | Segundo panel de tareas de la tienda en línea. |
| **ServiceTask3** | Tercer panel de tareas de la tienda en línea.  |



 

El código de la página web debe especificar un valor [para External.SelectedTaskPane](external-selectedtaskpane.md) al cargar para asegurarse de que el botón del panel de tareas correcto está resaltado una vez completada la navegación.

## <a name="examples"></a>Ejemplos

En el código de ejemplo siguiente se **muestra cómo NavigateTaskPaneURL** crea la dirección URL de la página web que se va a mostrar **para ServiceTask1.**

Ejemplo del **elemento Navigate:**


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Llamada de ejemplo al **método NavigateTaskPaneURL:**


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Ejemplo de dirección URL resultante usada para la página web que se muestra **en ServiceTask1:**


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/>                                        |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External.SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





