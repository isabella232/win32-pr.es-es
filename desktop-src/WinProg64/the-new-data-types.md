---
title: Los nuevos tipos de datos
description: Se introdujeron tres clases de tipos de datos para tipos de datos de precisión fija de Windows de 64 bits, tipos de precisión de puntero y tipos de precisión de puntero específico.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, tipos de datos
- tipos de datos de la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cf5960b5344da1d459d12dee96a2f67f2cfbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359334"
---
# <a name="the-new-data-types"></a>Los nuevos tipos de datos

Se introdujeron tres clases de tipos de datos para Windows de 64 bits: tipos de datos de precisión fija, tipos de precisión de puntero y tipos de precisión de puntero específico. Estos tipos se agregaron al entorno de desarrollo para que los desarrolladores puedan prepararse para Windows de 64 bits. Estos tipos se derivan del entero básico del lenguaje C y de los tipos largos. Por lo tanto, puede usar estos tipos de datos en el código que compile y pruebe en Windows de 32 bits y, a continuación, vuelva a compilar con el compilador de 64 bits cuando el destino sea Windows de 64 bits.

Incluso en el caso de las aplicaciones destinadas solo a Windows de 32 bits, la adopción de estos nuevos tipos de datos hace que el código sea más sólido. Para usar estos tipos de datos, debe analizar el código para ver el uso de punteros potencialmente no seguros, el polimorfismo y las definiciones de datos. Por ejemplo, cuando una variable es de tipo **ULong \_ ptr**, es evidente que se utilizará para convertir los punteros para las operaciones aritméticas o el polimorfismo. No es posible indicar este uso directamente mediante el uso de los tipos de datos más antiguos. (Puede hacerlo indirectamente mediante el uso de nombres de tipo derivado o la notación húngara, pero ambas técnicas son propensas a errores).

Todos estos tipos de datos se declaran en BaseTsd. h. Para obtener más información, incluidas las definiciones de estos tipos de datos, vea [tipos de datos de Windows](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Precisión fija

Los tipos de datos de precisión fija tienen la misma longitud en Windows de 32 y 64 bits. Para ayudarle a recordar esto, su precisión es parte del nombre del tipo de datos. A continuación se muestran los tipos de datos de precisión fija.



| Término                                                                       | Descripción                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | Entero de 32 bits sin signo<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | Entero de 64 bits sin signo<br/> |
| <span id="INT32"></span><span id="int32"></span>**INT32**<br/>       | Entero de 32 bits con signo<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | Entero de 64 bits con signo<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | Entero de 32 bits con signo<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | Entero de 64 bits con signo<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | Unsigned **INT32**<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | Unsigned **INT64**<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**ULONG32**<br/> | Unsigned **LONG32**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | Unsigned **LONG64**<br/>     |



 

## <a name="pointer-precision"></a>Precisión del puntero

A medida que cambia la precisión del puntero (es decir, a medida que se convierte en 32 bits en Windows de 32 bits y 64 bits con ventanas de 64 bits), los tipos de datos de precisión del puntero reflejan la precisión en consecuencia. Por lo tanto, es seguro convertir un puntero a uno de estos tipos al realizar la aritmética de punteros; Si la precisión del puntero es de 64 bits, el tipo es de 64 bits. Los tipos de recuento también reflejan el tamaño máximo al que puede hacer referencia un puntero. A continuación se muestran los tipos de precisión de puntero y de recuento.



| Término                                                                              | Descripción                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**DWORD \_ ptr**<br/> | Tipo Long sin signo para la precisión del puntero.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**MEDIO \_ ptr**<br/>    | La mitad del tamaño de un puntero. Use dentro de una estructura que contenga un puntero y dos campos pequeños.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**INT \_ ptr**<br/>       | Tipo de entero con signo para la precisión del puntero.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**LONG \_ ptr**<br/>    | Tipo Long con signo para la precisión del puntero.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**TAMAÑO \_ T**<br/>          | Número máximo de bytes a los que puede hacer referencia un puntero. Se usa para un recuento que debe abarcar el intervalo completo de un puntero.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | Tamaño con signo **\_ T**.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**\_ptr UHALF**<br/> | Unsigned **medio \_ ptr**.<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**UINT \_ ptr**<br/>    | Unsigned **int \_ ptr**.<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**ULONG \_ ptr**<br/> | **\_ Ptr largo** sin signo.<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Tipos de Pointer-Precision específicos

Los siguientes nuevos tipos de puntero ajustan explícitamente el puntero. Tenga cuidado al usar punteros en el código de 64 bits: Si declara el puntero con un tipo de 32 bits, el sistema operativo crea el puntero truncando un puntero de 64 bits. (Todos los punteros son de 64 bits en Windows de 64 bits).



| Término                                                                                 | Descripción                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**PUNTERO \_ 32**<br/> | Puntero de 32 bits. En Windows de 32 bits, se trata de un puntero nativo. En Windows de 64 bits, se trata de un puntero de 64 bits truncado.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**PUNTERO \_ 64**<br/> | Puntero de 64 bits. En Windows de 64 bits, se trata de un puntero nativo. En Windows de 32 bits, se trata de un puntero de 32 bits con signo extendido. <br/> Tenga en cuenta que no es seguro asumir el estado del bit de puntero alto.<br/> |



 

 

