---
title: TB_SETPRESSEDIMAGELIST mensaje (Commctrl.h)
description: Establece la lista de imágenes que usa la barra de herramientas para mostrar los botones que están en estado presionado.
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- TB_SETPRESSEDIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166570"
---
# <a name="tb_setpressedimagelist-message"></a>Mensaje \_ SETPRESSEDIMAGELIST de TB

Establece la lista de imágenes que usa la barra de herramientas para mostrar los botones que están en estado presionado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la lista de imágenes. Si solo usa una lista de imágenes, establezca este parámetro en cero. Consulte Comentarios para obtener más información sobre el uso de varias listas de imágenes.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se establecerá. Si este parámetro es **NULL,** no se muestra ninguna imagen en los botones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes que se usó anteriormente para mostrar los botones en su estado presionado, o **NULL** si no se estableció previamente ninguna lista de imágenes.

## <a name="remarks"></a>Observaciones

> [!Note]  
> La aplicación es responsable de liberar la lista de imágenes después de destruir la barra de herramientas.

 

El **mensaje \_ SETPRESSEDIMAGELIST de TB** no se puede combinar con TB [**\_ ADDBITMAP**](tb-addbitmap.md). Tampoco se puede usar con barras de herramientas creadas [**con CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), que llama a **TB \_ ADDBITMAP internamente.** Al crear una barra de herramientas con **CreateToolbarEx** o usar **TB \_ ADDBITMAP para** agregar imágenes, la barra de herramientas administra la lista de imágenes internamente. El intento de modificarlo con **TB \_ SETPRESSEDIMAGELIST** tiene consecuencias imprevisibles.

Las imágenes de botón no deben proceder de la misma lista de imágenes. Para usar varias listas de imágenes para las imágenes de botón de la barra de herramientas:

1.  Habilite varias listas de imágenes mediante el envío del control de barra de herramientas de un mensaje [**\_ DE CCM SETVERSION**](ccm-setversion.md) con *wParam* (el número de versión) establecido en 5.
2.  Para cada lista de imágenes que quiera usar, envíe al control de barra de herramientas **un mensaje \_ SETPRESSEDIMAGELIST de** TB. Establezca *wParam en* un valor *wParam* definido por la aplicación que se usará para identificar la lista. Establezca *lParam en* el identificador HIMAGELIST de la lista.
3.  Para cada botón, establezca el miembro **iBitmap** de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del botón en MAKELONG(*iIndex*, *iImageID*). El *valor de iImageID* es el identificador de la lista de imágenes adecuada que se definió en el paso dos. El *valor iIndex* es el índice de la imagen determinada dentro de esa lista.
4.  Agregue los botones enviando al control de barra de herramientas [**un mensaje \_ ADDBUTTONS de TB.**](tb-addbuttons.md)

En el fragmento de código siguiente se muestra cómo agregar cinco botones a una barra de herramientas, con imágenes de tres listas de imágenes diferentes. La compatibilidad con varias listas de imágenes está habilitada con un [**\_ mensaje SETVERSION de CCM.**](ccm-setversion.md) A continuación, las listas de imágenes se establecen y asignan los IDs de 0 a 2. A los botones se les asignan imágenes de las listas de imágenes como se indica a continuación:

-   El botón 0 es de la lista de imágenes cero (ahim \[ \] 0) con el índice 1.
-   El botón 1 es de la lista de imágenes uno (ahim \[ \] 1) con un índice de 1.
-   El botón 2 es de la lista de imágenes dos (ahim \[ \] 2) con un índice de 1.
-   El botón 3 es de la lista de imágenes cero (ahim \[ \] 0) con un índice de 2.
-   El botón 4 es de la lista de imágenes uno (ahim \[ \] 1) con un índice de 3.

Por último, los botones se agregan al control de barra de herramientas con un [**\_ mensaje ADDBUTTONS de**](tb-addbuttons.md) TB.


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TB \_ GETPRESSEDIMAGELIST**](tb-getpressedimagelist.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

