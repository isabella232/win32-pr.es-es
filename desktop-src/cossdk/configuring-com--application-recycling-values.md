---
description: Puede usar los métodos siguientes para configurar los valores de reciclaje de la aplicación para la aplicación COM+.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Configuración de los valores de reciclaje de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153467"
---
# <a name="configuring-com-application-recycling-values"></a>Configuración de los valores de reciclaje de aplicaciones COM+

Puede usar los métodos siguientes para configurar los valores de reciclaje de la aplicación para la aplicación COM+.

> [!Note]  
> No se puede reciclar una aplicación COM+ que se ha configurado para ejecutarse como un servicio de Windows. Además, las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

Para configurar el reciclaje de aplicaciones para una aplicación COM+, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en la aplicación de servidor COM+ que desea reciclar y, a continuación, haga clic en **propiedades**.

2.  En la pestaña **agrupación & reciclaje** , escriba los valores de **límite de duración (minutos)**, límite de **memoria (KB)**, **tiempo de espera de expiración (minutos)**, **límite de llamadas** y **límite de activaciones**, en función de los criterios que desee utilizar.

    -   **Límite de duración** indica el número máximo de minutos que puede ejecutarse un proceso antes de que se recicle. El intervalo válido es de 0 a 30.240 minutos (21 días). El número predeterminado de minutos es 0.
    -   **Límite de memoria** indica la cantidad máxima de uso de memoria de proceso (en kilobytes) antes de reciclar el proceso. Si el uso de memoria del proceso excede el número especificado durante más de un minuto, el proceso se recicla. El intervalo válido es de 0 a 1.048.576 KB y el uso de memoria predeterminado es de 0 KB.
    -   El **tiempo de espera de expiración** indica el número de minutos que se debe esperar antes de que se cierre forzosamente, para la liberación de todas las referencias externas a los objetos del proceso. El intervalo válido es de 1 a 1440 minutos (24 horas) y el tiempo de espera de expiración predeterminado es 15 minutos. Este valor sólo se usa cuando ya se ha determinado que un proceso se reciclará en función de otros criterios.
    -   **Límite de llamadas** indica el número máximo de llamadas que los objetos de aplicación pueden aceptar antes de reciclar el proceso. El intervalo válido es de 0 a 1.048.576 llamadas y el número predeterminado de llamadas es 0.
    -   **Límite de activación** indica el número máximo de activaciones de objetos de aplicación que se aceptan antes de reciclar el proceso. El intervalo válido es de 0 a 1.048.576 activaciones y el número predeterminado de activaciones es 0.

    > [!Note]  
    > Cuando el valor de límite de **duración**, **límite de memoria**, **límite de llamadas** o límite de **activación** se establece en 0 (el valor predeterminado), se deshabilita el reciclaje de la aplicación para ese criterio. Cuando los cuatro criterios se establecen en 0, el reciclaje de la aplicación está deshabilitado para la aplicación seleccionada.

     

3.  Haga clic en **OK**.

## <a name="visual-basic"></a>Visual Basic

La siguiente función de Microsoft Visual Basic muestra cómo puede establecer los valores de reciclaje de la aplicación para cualquier aplicación de servidor COM+ que elija. Para usarlo desde Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+.


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Para usar la función, proporcione un valor de cadena para el nombre de la aplicación y valores enteros para la configuración de reciclaje de la aplicación deseada. En el siguiente código de Visual Basic se muestra cómo establecer el valor de **RecycleLifetimeLimit** en 5, el valor de **RecycleMemoryLimit** en 10, el valor de **RecycleCallLimit** en 9, el valor de **RecycleActivationLimit** en 100 y el valor de **RecycleExpirationTimeout** en 15.


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de reciclaje de aplicaciones COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



