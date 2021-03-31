---
title: Reglas para usar punteros
description: Trasladar el código para compilar para Windows de 32 y 64 bits es sencillo. Solo necesita seguir unas cuantas reglas simples sobre cómo convertir punteros y usar los nuevos tipos de datos en el código. Las reglas para la manipulación de puntero son las siguientes.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- reglas para usar los punteros programación de Windows de 64 bits
- manipulación de puntero de 64 programación de Windows de bits
- convertir punteros en programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103995699"
---
# <a name="rules-for-using-pointers"></a>Reglas para usar punteros

Trasladar el código para compilar para Windows de 32 y 64 bits es sencillo. Solo necesita seguir unas cuantas reglas simples sobre cómo convertir punteros y usar los nuevos tipos de datos en el código. Las reglas para la manipulación de puntero son las siguientes.

1.  No convierta punteros a **int**, **Long**, **ULong** o **DWORD**.

    Si debe convertir un puntero para probar algunos bits, establecer o borrar bits o manipular de otro modo su contenido, use el tipo **uint \_ ptr** o **int \_ ptr** . Estos tipos son tipos enteros que se escalan al tamaño de un puntero para Windows de 32 y 64 bits (por ejemplo, **ULong** para windows de 32 bits y \_ Int64 para Windows de 64 bits). Por ejemplo, suponga que está migrando el código siguiente:

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    Como parte del proceso de portabilidad, cambiaría el código como se indica a continuación:

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    Use **uint \_ ptr** e **int \_ ptr** cuando sea apropiado (y, si no está seguro de si son necesarios, no hay ningún daño en su uso en caso de que se produzcan). No convierta los punteros a los tipos **ULong**, **Long**, **int**, **uint** o **DWORD**.

    Tenga en cuenta que el **identificador** se define como un valor **\* nulo**, por lo que conversión un valor de **identificador** a un valor **ULong** para probar, establecer o borrar los bits de orden inferior 2 es un error en Windows de 64 bits.

2.  Utilice la función **PtrToLong** o **PtrToUlong** para truncar los punteros.

    Si debe truncar un puntero a un valor de 32 bits, utilice la función **PtrToLong** o **PtrToUlong** (definida en Basetsd. h). Estas funciones deshabilitan la advertencia de truncamiento de puntero mientras dure la llamada.

    Use estas funciones con cuidado. Después de convertir una variable de puntero mediante una de estas funciones, no la use nunca como un puntero de nuevo. Estas funciones truncan los 32 bits superiores de una dirección, que normalmente son necesarios para tener acceso a la memoria a la que se hace referencia originalmente mediante un puntero. El uso de estas funciones sin mucha consideración dará como resultado código frágil.

3.  Tenga cuidado al usar \_ valores de puntero 32 en el código que se puede compilar como código de 64 bits. El compilador firmará el puntero cuando se asigne a un puntero nativo en el código de 64 bits, no extiende el puntero a cero.
4.  Tenga cuidado al usar \_ valores de puntero 64 en el código que se puede compilar como código de 32 bits. El compilador firmará el puntero en el código de 32 bits, no extiende a cero el puntero.
5.  Tenga cuidado al usar los parámetros OUT.

    Por ejemplo, supongamos que tiene una función definida de la siguiente manera:

    `void func( OUT PULONG *PointerToUlong );`

    No llame a esta función como se indica a continuación.

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    En su lugar, utilice la siguiente llamada.

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    Conversión &UL a **PULONG \*** evita un error del compilador, pero la función escribirá un valor de puntero de 64 bits en la memoria en &UL. Este código funciona en Windows de 32 bits, pero producirá daños en los datos en Windows de 64 bits y será sutil y difícil de encontrar. La línea inferior: no reproduzca trucos con el código de C: es mejor y sencillo.

6.  Tenga cuidado con las interfaces polimórficas.

    No cree funciones que acepten parámetros **DWORD** para datos polimórficos. Si los datos pueden ser un puntero o un valor entero, use el \_ tipo uint PTR o **PVOID** .

    Por ejemplo, no cree una función que acepte una matriz de parámetros de excepción con el tipo de valores **DWORD** . La matriz debe ser una matriz de valores **DWORD \_ ptr** . Por lo tanto, los elementos de la matriz pueden contener direcciones o valores enteros de 32 bits. (La regla general es que si el tipo original es **DWORD** y debe ser el ancho del puntero, conviértalo en un valor de **DWORD \_ ptr** . Esa es la razón por la que hay tipos de precisión de puntero correspondientes). Si tiene código que usa **DWORD**, **ULong** u otros tipos de 32 bits de forma polimórfica (es decir, desea que el parámetro o el miembro de estructura contengan una dirección), use **uint \_ ptr** en lugar del tipo actual.

7.  Use las nuevas funciones de clase de ventana.

    Si tiene datos privados de ventana o clase que contienen punteros, el código deberá usar las siguientes funciones nuevas:

    -   [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    Estas funciones se pueden usar en Windows de 32 y 64 bits, pero son necesarias en Windows de 64 bits. Prepárese para la transición mediante el uso de estas funciones ahora.

    Además, debe tener acceso a los punteros o a los identificadores de los datos privados de la clase mediante las nuevas funciones en Windows de 64 bits. Para ayudarle a encontrar estos casos, los siguientes índices no se definen en Winuser. h durante una compilación de 64 bits:

    -   GWL \_ WndProc
    -   GWL \_ hInstance
    -   GWL \_ HWDPARENT
    -   GWL \_ USERDATA

    En su lugar, Winuser. h define los nuevos índices siguientes:

    -   GWLP \_ WndProc
    -   GWLP \_ hInstance
    -   GWLP \_ HWNDPARENT
    -   GWLP \_ USERDATA
    -   identificador de GWLP \_

    Por ejemplo, el código siguiente no se compila:

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    Debe cambiarse de la siguiente manera:

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    Al establecer el miembro **cbWndExtra** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , asegúrese de reservar espacio suficiente para los punteros. Por ejemplo, si está reservando bytes de tamaño (DWORD) para un valor de puntero, Reserve bytes de tamaño (DWORD \_ ptr).

8.  Acceder a todos los datos de ventana y de clase mediante el **\_ desplazamiento de campo**.

    Es habitual tener acceso a los datos de la ventana mediante desplazamientos codificados de forma rígida. Esta técnica no es portable a Windows de 64 bits. Para que el código sea portátil, acceda a los datos de la ventana y de la clase mediante la macro de **\_ desplazamiento de campo** . No asuma que el segundo puntero tiene un desplazamiento de 4.

9.  Los tipos **lParam**, **wParam** y **LRESULT** cambian el tamaño con la plataforma.

    Al compilar código de 64 bits, estos tipos se expanden hasta 64 bits, porque normalmente contienen punteros o tipos enteros. No mezcle estos valores con los valores **DWORD**, **ULong**, **uint**, **int**, **int** o **Long** . Examine cómo se usan estos tipos y asegúrese de que no trunca accidentalmente los valores.

 

 